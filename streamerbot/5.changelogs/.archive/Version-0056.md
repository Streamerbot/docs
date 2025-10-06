---
title: Version 0.0.56
description: 
published: true
date: 2023-06-11T15:04:44.798Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:36:28.010Z
---

* Misc fixes/updates
* Fix for IsSourceVisible not returning a value (woops)
* Fix not being able to delete a file in file watcher
* Handle a potential error in audio playback (from malformed audio, or wrong audio types)
* Fixed a crash when editing some reward sub-actions when there are no rewards
* Fix Logic > If when action is deleted, trying to edit will cause it to crash
{.changelog-fixes}

<span></span>

* Twitch emote urls have been updated to new cdn, so animated emotes will show if used
* OBS Set Source Visibility has been changed to a state, and will auto update settings
* SLOBS Set Source Visibility has been changed to a state, and will auto update settings
* Twitch Message sub-actions will now show part of the message to be sent in the sub action list
* Update AddTargetInfo sub-action to overwrite values if they already exist, so it can be run multiple times
{.changelog-updates}

<span></span>

* Add new capability to get your clips, this functionality is reserved for Execute C# at the moment, and a basic example will be provided
* Add new [WebSocket Server Request](/Servers-Clients/WebSocket-Server/Requests), `GetActiveViewers`
* Add new option to LogicIf, DoAction and C# Run Action, you can now run the action immediately (inline), or queue it so it runs in its set queue
{.changelog-new}

## LogicIf, DoAction, C# RunAction Update
Before, when using any of these sub-actions, running an action would just run it inline, as if it was just a sub-action.  With this update, a new option has been added to all of these `Run Immediately` which is selected by default.

What this will do, is it will let you re-queue the action, so it can run in the queue thats it's setup to use.  So say you have a logic if that runs in a non-blocking queue, but it will run an action that is normally in a blocking queue.  The default behaviour is, the action will run as-if its in a non-blocking queue because its parent action is.  If you were to uncheck this setting, it would then re-queue the action into its blocking queue, and run from there.

Some side effects from this usage.  For those that use the default, nothing will change.  If you start letting actions be requeued this can cause an out of order running of actions because once its re-queued its essentially completely detached from the action that ran it.  This also means, if there are any actions that follow, they will happen without waiting, also, any changes that the action does to the arguments, won't persist through.

## WebSocket Server Request - GetActiveViewers
By sending a request to get active viewers, you can retrieve what Streamer.bot shows as an active viewer, this will match what shows up in the user list of the bot's window.

Response

```json
{
    "id": "1",
    "count": 1,
    "viewers": [
        {
            "id": 0000,
            "login": "<login>",
            "display": "<dispaly>",
            "subscribed": true,
            "role": "Broadcaster",
            "groups": [
                "regulars"
            ],
            "channelPointsUsed": 62652,
            "lastActive": "2021-07-10T09:27:53.8818207-04:00",
            "exempt": false
        }
    ],
    "status": "ok"
}
```

## Twitch Clips
You can now retrieve a list of your Twitch clips, and do with them as you wish.  Make a !randomclip command, that'll get your clips and output to chat a random clip, or by way of some HTML magic, have it play in OBS.

A note on the these methods, since they get all clips, I would recommend having some sort of caching mechanism built into your C# code so the apis are not constantly hit if multiple looks are made.  The chances of new clips being added are relatively low, so going this route is preferred.  The examples provided don't do caching, but I'll gladly help with that if desired.

There are 2 new methods available for the Execute C# Code sub-action

```csharp
List<ClipData> GetAllClips();
List<ClipData> GetClipsForGame(int gameId);
List<ClipData> GetClipsForUser(int userId);
List<ClipData> GetClipsForUser(string username);
```

Example Execute C# Code:

**NOTE** You will need to add `C:\Windows\Microsoft.NET\Framework\v4.0.30319\\System.Core.dll` as a reference

```csharp
using System;
using System.Linq;

public class CPHInline
{
	public bool Execute()
	{
		// get all clips from twitch, can also get by Game ID
		var allClips = CPH.GetAllClips();

		// if no clips, stop processing anymore actions
		if (allClips.Count == 0) return false;

		// pick a random clip
		var randomClip = allClips.OrderBy(c => Guid.NewGuid()).First();

		// send a message to chat with the random clip
		CPH.SendMessage($"Random Clip! {randomClip.Title}");
		CPH.SendMessage($"{randomClip.Url}");

		// set some data in the arguments, for any subaction to use
		CPH.SetArgument("randomClipTitle", randomClip.Title);
		CPH.SetArgument("randomClipUrl", randomClip.Url);
		CPH.SetArgument("randomClipDuration", randomClip.Duration);
		CPH.SetArgument("randomClipBroadcaster",randomClip.BroadcasterName);
		CPH.SetArgument("randomClipCreator", randomClip.CreatorName);
		CPH.SetArgument("randomClipViewCount", randomClip.ViewCount);
		CPH.SetArgument("randomClipThumbnailUrl", randomClip.ThumbnailUrl);

		return true;
	}
}
```

Example code for taking a username from command input

```csharp
using System;
using System.Linq;

public class CPHInline
{
	public bool Execute()
	{
		var userName = args["rawInput"].ToString();

		// get all clips from twitch, can also get by Game ID
		var allClips = CPH.GetClipsForUser(userName);

		// if no clips, stop processing anymore actions
		if (allClips.Count == 0) return false;

		// pick a random clip
		var randomClip = allClips.OrderBy(c => Guid.NewGuid()).First();

		// send a message to chat with the random clip
		CPH.SendMessage($"Random Clip for {userName}! {randomClip.Title}");
		CPH.SendMessage($"{randomClip.Url}");

		// set some data in the arguments, for any subaction to use
		CPH.SetArgument("randomClipTitle", randomClip.Title);
		CPH.SetArgument("randomClipUrl", randomClip.Url);
		CPH.SetArgument("randomClipDuration", randomClip.Duration);
		CPH.SetArgument("randomClipBroadcaster",randomClip.BroadcasterName);
		CPH.SetArgument("randomClipCreator", randomClip.CreatorName);
		CPH.SetArgument("randomClipViewCount", randomClip.ViewCount);
		CPH.SetArgument("randomClipThumbnailUrl", randomClip.ThumbnailUrl);

		return true;
	}
}
```

ClipData contains the following values

```csharp
string Id;
string Url;
string EmbedUrl;
int BroadcasterId;
string BroadcasterName;
int CreatorId;
string CreatorName;
string VideoId;
string GameId;
string Language;
string Title;
int ViewCount;
DateTime CreatedAt;
string ThumbnailUrl;
float Duration;
```

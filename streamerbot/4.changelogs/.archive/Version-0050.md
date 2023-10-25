---
title: Version 0.0.50
description: 
published: true
date: 2023-06-11T15:12:39.467Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:36:03.945Z
---

First off, Happy Birthday ChannelPointsHandler, you turned 1 on June 16th 2021, and as a celebration, a massive update, packed with new features and fixes all around.

Thank you everyone for deciding to use this piece of software that I write in my spare time, and sometimes, don't update for months 😄 This community has been something special, and is very dear to my heart.  The VR community at large has had such an impact on me that I can't begin to thank you all enough for. From landing a job at a VR company (LIV), to finding that someone special in my life (Lithaya, if I may, I'd like to dedicate this release to you), and for many great friends along the way.

My DMs are always open, and, I don't bite (well, I try not to); while I may seem like I'm super busy all the time, you might be surprised, I do like playing games or anything else at times to 😄 

While I was waiting for the UI update for the next part, I thought maybe it was time to accelerate the renaming of ChannelPointsHandler, since it has turned into sooo much more then just that.

So, I now give you...

[![Streamer.bot](https://user-images.githubusercontent.com/3193453/121985357-9c6fe500-cd62-11eb-9316-5cb66bc5b44b.png)](https://streamer.bot/)

One added note, since their have been quite a few asking about this, I have also setup a [Patreon](https://www.patreon.com/nate1280) which should be going live the same day as this release, and will likely be evolving a bit over the next month as I try to figure things out.

* Miscellaneous fixes
* Fixes to credits
* Execute C# code wasn't returning result
* Fix some potential crashes originating from speech to text if its not present
* Fix/update import/export to properly handle Execute C# Code/Method actions
* Fix editing reward, certain values were not cleared
* Fix creating/editing channel rewards
* Fix Reward Set Cost sub-action
* Fix OBS Set Browser Source, invalid URLs would crash, taking down the queue they were running from
* Should no longer crash when you enter an invalid color when creating rewards
* Make queues a bit more resilient to crashes
{.changelog-fixes}

<span></span>

* Only show errors when using Execute C# code, ignores warnings now
* Removed peak meter from speech to text tab
* Update commands to have more sources for triggering, they can be activated from sub and resub messages, new commands will default to message sources
* Overhaul of certain thread related specifics, tldr; speedier, improvements all around
* Resizable window
* Rewrote Twitch API handling
* General performance improvements
* Pass along the user's color in twitch messages and some relevant events
* Update how cheers are handled, this means the loss of the `totalBits` variable, but full emote support and more has been gained
{.changelog-updates}

<span></span>

* Add auto reconnect option for twitch
* Add new [HTTP Server](#http-server)
* Add new event, present viewers
* Add new sub-action to set a scene's filter state
* Add support for [Streamlabs!](#streamlabs)
* Add new [Message event](#new-message-event)
* Add support for [Twitch Polls and Predictions!](#twitch-polls-and-predictions)
* Add new sub-action to pause action queues, as well as accompanying Execute C# methods
* Added support for another streaming app, [SLOBS!](#slobs-support)
{.changelog-new}

## Plugins
There is even a TouchPortal plugin built to support Streamer.bot! A StreamDeck plugin is also in the works.

## Execute C# Code
There is a new method that can be used:
```csharp
bool ExecuteMethod(string executeCode, string methodName);
```
Can be used to execute a method from another C# code action

## New Events
### Twitch - Present Viewers
Internally the bot has an event that fires every 5 minutes to get a list of viewer that are present in your channel, I have exposed this event, primarily for use in Execute C#, so you can write your own script for points tracking, and a full system surrounding that. An example of this may come later.

### Streamlabs - Donations
Much like twitch cheers, you can attach events for when someone donates to you. Say someone donates $6.66 well, you can now perform actions on specific amounts, ranges, or just in general. Note, the amount is in whatever currency your Streamlabs is setup to handle (or should be)

### Streamlabs - Merchandise Purchase
Do you host a merch store through Streamlabs, well, you can add an event when someone buys a t-shirt, or a fancy new mouse pad, or any other item that might be in your store.

### Twitch - Poll Created/Updated/Completed
These events will allow you do actions for when polls are used, do something fancy when a poll is created to alert your viewers that something is happening. And/or do something when a poll is finished.

### Twitch - Prediction Created/Update/Locked/Resolved/Canceled
These events can all occur during a prediction, and much like the polls, can add a dynamic flair to your stream when they occur.

### Twitch - Message
This event will occur every time a message comes through on twitch (this does not include the cheer event). Add some level of interactivity when messages happen, and/or write your own HTML based chat!

## Credits
Added a new test credits method, can be called from the Websocket server, or from the HTTP listener

## HTTP Server
Added a new network service, HTTP listener. This will allow you to make HTTP calls to get certain data, and also to run actions.

See [HTTP Server](/Servers-Clients/HTTP-Server) for full details and usage of this new capability

## Streamlabs!
You can now connect to your Streamlabs account and get donation and merchandise purchase events. To configure this, you will need to obtain your socket api token, and set this within the settings. There is no sign in authorization to do this at the moment due to how long it takes to get this approved.

2 new events are added for Streamlabs, and they are also included in the Websocket broadcast

## SLOBS Support!
A new addition to Streamer.bot, you can now control SLOBS the same way you can control OBS! Feature set should be parity, along with a whole new slew of Execute C# code methods to use for it as well.

## Twitch Polls and Predictions!
Create and resolve twitch polls right from within the app; assign actions to the creation/updating/ending of a poll. These events can also be broadcasted across the websocket server so you can create dynamic webpages to use within OBS/SLOBS

## BTTV/FFZ/Cheermotes
BTTZ/FFZ have been integrated into the Twitch chat library, so along side emotes that are sent within a twitch message, positions and locations of BTTV/FFZ emotes are also determined and passed along.

A side effect of this update, Pyramids now support BTTV and FFZ emotes!

## New Message Event!
Added a new event for all messages that come through Twitch, in combination with the BTTV/FFZ change, all relevant message data is now sent across in the websocket broadcasts. There is also a spot to assign actions to, but due to the nature of this event, I would highly recommend only an Execute C# action be used with it, as it will require more parsing then what is capable with the basic sub-actions.

# More New Execute C# Methods
## For OBS:
```csharp
bool ObsIsFilterEnabled(string scene, string filterName, int connection = 0)
```
## For Twitch Channel Rewards
```csharp
void UpdateRewardCooldown(string rewardId, int cooldown, bool additive = false);
```
## For Slobs:
```csharp
bool SlobsIsConnected(int connection = 0);
bool SlobsConnect(int connection = 0);
void SlobsDisconnect(int connection = 0);
bool SlobsIsStreaming(int connection = 0);
void SlobsStopStreaming(int connection = 0);
void SlobsStartStreaming(int connection = 0);
bool SlobsIsRecording(int connection = 0);
void SlobsStartRecording(int connection = 0);
void SlobsStopRecording(int connection = 0);
void SlobsPauseRecording(int connection = 0);
void SlobsResumeRecording(int connection = 0);
void SlobsSetScene(string sceneName, int connection = 0);
string SlobsGetCurrentScene(int connection = 0);
bool SlobsIsSourceVisible(string scene, string source, int connection = 0);
void SlobsSetSourceVisibility(string scene, string source, bool visible, int connection = 0);
void SlobsShowSource(string scene, string source, int connection = 0);
void SlobsHideSource(string scene, string source, int connection = 0);
void SlobsHideGroupsSources(string scene, string groupName, int connection = 0);
string SlobsSetRandomGroupSourceVisible(string scene, string groupName, int connection = 0);
List<string> SlobsGetGroupSources(string scene, string groupName, int connection = 0);
void SlobsSetBrowserSource(string scene, string source, string url, int connection = 0);
void SlobsSetGdiText(string scene, string source, string text, int connection = 0);
bool SlobsIsFilterEnabled(string scene, string filterName, int connection = 0);
bool SlobsIsFilterEnabled(string scene, string source, string filterName, int connection = 0);
void SlobsSetFilterState(string scene, string filterName, int state, int connection = 0);
void SlobsSetFilterState(string scene, string source, string filterName, int state, int connection = 0);
void SlobsShowFilter(string scene, string filterName, int connection = 0);
void SlobsShowFilter(string scene, string source, string filterName, int connection = 0);
void SlobsHideFilter(string scene, string filterName, int connection = 0);
void SlobsHideFilter(string scene, string source, string filterName, int connection = 0);
void SlobsToggleFilter(string scene, string filterName, int connection = 0);
void SlobsToggleFilter(string scene, string source, string filterName, int connection = 0);
void SlobsSetRandomFilterState(string scene, int state, int connection = 0);
void SlobsSetRandomFilterState(string scene, string source, int state, int connection = 0);
void SlobsSetSourceMuteState(string scene, string source, int state, int connection = 0);
void SlobsSourceMute(string scene, string source, string filterName, int connection = 0);
void SlobsSourceUnMute(string scene, string source, string filterName, int connection = 0);
void SlobsSourceMuteToggle(string scene, string source, string filterName, int connection = 0);
```
## For Pausing Action Queues
```csharp
void PauseActionQueue(string name);
void PauseAllActionQueues();
void ResumeActionQueue(string name, bool clear = false);
void ResumeAllActionQueues(bool clear = false);
```
## Miscellaneous Methods
```csharp
List<Cheermote> GetCheermotes();
```
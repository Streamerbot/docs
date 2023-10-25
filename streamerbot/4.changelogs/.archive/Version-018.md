---
title: Version 0.1.8
description: Released 2022-06-01
published: true
date: 2023-04-28T18:13:41.043Z
tags: 
editor: markdown
dateCreated: 2023-04-28T18:13:38.326Z
---


* Misc fixes
* DonorDrive profile updated event was sending wrong websocket event type
* Updated the Action picker to show better message when there are no actions
* GetActionGroupState sub-action was configured wrong, also a settings upgrade to correct any existing sub-actions
* ObsSetReplayBufferState was starting/stopping stream, not the buffer
* ObsSetReplayBufferState had incorrect states
* Removal of channel reward from the UI should be working correctly now
* Get/Set Command State sub-actions would cause a crash if there are no commands
* Set Reward Cooldown sub-action would crash if no Twitch auth data was present
* OBS Set Audio Track state would toggle when explicitly setting active, this is a bug in obs-websocket 4.x, workaround applied
* The file selection button in the OBS Take Screenshot sub-action now works
* Date calculations for Follow Age Info sub-action are now correct
* Twitch Sub-Counter should no longer cause crashes if file/path is not found
* Can no longer rename a group to an empty string
* ObsSourceMute C# methods had an extra unused parameter, this has been removed
* OBS SetMediaSourceFile sub-action was not parsing scene and source names
* OBS SetImageSourceFile sub-action was not parsing scene and source names
* How play not found option works, was stopping the sound even if you were playing via default device
* Group collapsing for Actions
* Sub-action dragging to groups
* Max length for importing actions, there was a 32kb hard limit on the text box, it is now int.MaxValue
{.changelog-fixes}

<span></span>

* Vorbis library updated
* Read Random Line sub-action now has a count option, this will add however many lines count is, removing the need to add multiple sub-actions
* Update Twitch Timeout sub-action to be able to include a reason
* Some tabs related to specific Twitch features have been moved under the Twitch tab
* All streaming platforms have been moved to there own combined top level tab
* All broadcasting software tabs have been moved to there own combined top level tab
* All integrations have been moved to there own combined top level tab
* Commands have a new variable available, `%commandId%` which contains the ID of the command that was triggered, this applies for a cooldown action as well.
* Added a new variable `%userType%`, this will be present for any actions that adds user information to the arguments
* Broadcaster information and random users will no longer be added to every action, this is replaced by sub-actions for the various streaming services
* Add Target Info got a new target source, Broadcaster, which will add the broadcasters extended information to the arguments
* Requesting new [scopes for your Twitch account](#twitch-new-scopes)
* Some updates to the Sub-action context menu, slightly different behaviour and updated text
* Move some Twitch classes to a common library for better use within C# code, this may cause some breaking changes
* [StreamElements](#streamelements) now uses OAuth to access the service, you no longer need to enter your JWT token.
* File Watcher has been updated to support folder watching with filename filters
* Cleaned up how Tabs can me moved around and hidden, right click on a tab to bring up a context menu if they can be hidden
* Rename SLOBS to Streamlabs Desktop throughout the app
* Under the hood, actions have been moved to there own data file
* Minor tweaks to the way settings files are saved
* Export Actions list is now sorted alphabetically
* Remove big Twitch Connect button
* Action importing handles Execute C# Code sub-actions a bit better now, and is more intelligent on how references are handled
* Various libraries updated
* Change default options when creating a Wasapi device for the default device, now matches specific device creation
* Alter how device selection works when overriding device in Play Sound and Play Sound from Folder sub-actions
* Moved save button to a toolbar at the top of the main window
* Moved import/export to buttons on the toolbar, and removed them from the actions context menu
{.changelog-updates}

<span></span>

* Add Twitch First Time Chat indicator, there is a new argument for messages `%firstMessage%`, this is a boolean, true or false
* Wildcard can be used when subscribing to websocket events
* New sub-action [Add Team Info](#add-team-info), can get team information for a user
* ObsRaw has a new option to not add return data to the argument stack; the raw JSON will still be added.  This defaults to true to prevent breaking of existing actions
* New sub-action [Obs Hide Scene Sources](#obs-hide-scene-sources) and C# method to hide all the sources of a scene, this is the same behaviour as Obs Hide Group Sources, except for scenes.
* New sub-action [Obs Set Random Scene Source Visible](#obs-set-random-scene-source-visible) and C# method to set a random source in a scene to visible, this is the same behaviour as Obs Set Random Group Source visible, except for scenes.
* Provided as a 64-bit build
* [YouTube](#youtube-integration) has been added and is currently a WIP and is being tested.
* Added a new C# method to run an action by it's id `RunActionById(string actionId, bool runImmediately = true)`
* New sub-action [Add Broadcaster Information](#add-twitch-broadcaster-information), to add the broadcaster's information to arguments
* New sub-action [Add Random Users](#add-random-twitch-users), to add a specific number of random Twitch users to the arguments
* Parse the subscription length from Twitch messages and pass that information forward, will be added as `%monthsSubscribed%` if it is greather then 0
* Sub-actions can now be enabled/disabled, disabled sub-actions are marked as red in the list
* Added new [C# methods](#new-c-methods)
* Now parsing the badge-info tag from Twitch chat, and passing the subscriber duration along
* The `Ignore Bot` flag for commands now takes into account if the bot account is the same as the broadcaster account and does nothing instead of ignoring, applies to Twitch only
* VoiceMod integration! Control VoiceMod from **Streamer.bot**
* Direct [Pulsoid integration](#pulsoid-integration)
* Direct [HypeRate integration](#hyperate-integration)
* [OBS Connections](#obs-connections) can be flagged as default, and/or forced.
* New sub-action [Set Voice Control Command State](#set-voice-control-command-state) to set the state of a Voice Control Command
* New sub-action [Set Voice Control Command](#set-voice-control-command) to set the command of an anywhere type Voice Control Command
* Integration with [PolyPop](#polypop-integration)
* Messages sent via the broadcaster to twitch are now looped back to itself with emote parsing in tow
* Twemoji parsing for Twitch messages, this will parse Unicode emotes to images
* Broadcaster information is auto added for certain events where a source is known
* A new authorization success page will show, instead of a single line of text
* Twitch/YouTube message sub-actions support multi-line, dialogs have been updated as well
* Add new GetBroadcaster request to websocket
* Add new GetBroadcaster endpoint to http server
* Add new Broken event to Pyramids
* New event for StreamElements, Merch, trigger actions from merchandise purchases
* [Action Queues](#action-queues), you can now see actions running in realtime, and see a history of them
* [Streamer.bot](#streamerbot-website-integration) Website integration
* Integration with [Kofi](#kofi-integration)
* Integration with [Patreon](#patreon-integration)
* Added C# Compiler settings, specifically, you can add common references that will be included with all Execute C# Code sub-actions
* Custom C# libraries used as references, can now be places in a dlls subfolder
* Added the StreamElements merch event
* Twitch Badges are now parsed and added as arguments for relevant events
* Integration with [TipeeeStream](#tipeestream-integration)
* Integration with [TreatStream](#treatstream-integration)
* Added new Log sub-action, to allow logging from within an action
* Execute C# Code window sizing is saved now, it will open at the last used size
* Add selected file information to arguments for Play Sound from Folder sub-action; %randomSoundFile% contains the full path of the file and %randomSoundFileName% contains just the file name
* Commands can be imported/exported along side actions
* In Execute C# Code window, you can right click to copy the compile log to clipboard
* Add filtering to Actions list, this will only filter on the action name at the moment
* Add filtering to Commands list, this will only filter on the command at the moment
* Add filtering to Action selection dialog, this will only filter on the action name at the moment
{.changelog-new}

## YouTube Integration

Probably one of the most requested features has finally been added, more details will be added to this section over the next few days.

You'll be able to authorize with your YouTube account, and monitor chat, giving you the ability to react to chat messages, super chat, super stickers and more!

More information will follow!

See [YouTube](/Platforms/YouTube) for information on how to get started!

## 64-bit Build

Moving forward, **Streamer.bot** will be offered in a 64-bit build, as opposed to a 32-bit build. This opens up the ability to interface with more librariries and tools using the integrated C# capabilities.

## Twitch New Scopes

When you connect with your broadcaster account, the following new scopes will be requested

* `moderator:manage:banned_users`
* `moderator:read:blocked_terms`
* `moderator:manage:blocked_terms`
* `moderator:manage:automod`
* `moderator:read:automod_settings`
* `moderator:manage:automod_settings`
* `moderator:read:chat_settings`
* `moderator:manage:chat_settings`
* `whispers:edit`
* `user:read:follows`
{.grid-list}

Since I needed to add the moderation scopes, I decided to finally add the whisper edit scope, this will allow the broadcaster account to send whispers.  The restrictions by twitch are still in place!

## New C# Methods

Add the following new C# methods

### User Variables
```csharp
T GetTwitchUserVar<T>(string userName, string varName, bool persisted = true);
T GetYouTubeUserVar<T>(string userName, string varName, bool persisted = true);
void SetTwitchUserVar(string userName, string varName, object value, bool persisted = true);
void SetYouTubeUserVar(string userName, string varName, object value, bool persisted = true);
void UnsetTwitchUserVar(string userName, string varName, bool persisted = true);
void UnsetYouTubeUserVar(string userName, string varName, bool persisted = true);
void UnsetTwitchUser(string userName, bool persisted = true);
void UnsetYouTubeUser(string userName, bool persisted = true);
```

### YouTube Methods
```csharp
void SendYouTubeMessage(string message);
```

### Actions

```csharp
bool RunActionById(string actionId, bool runImmediately = true);
```

### Websocket Custom Servers

```csharp
int WebsocketCustomServerGetConnectionByName(string name);
```

## OBS Connections

OBS connections have 2 new properties in the context menu when you <kbd>Right-click</kbd> on them, Default and Forced.

Setting a connection to default means if the OBS Websocket an OBS sub-action is using is not found, it will use the default selected OBS connection.

Setting a connection to forced, will override all OBS sub-actions and OBS C# methods to use this connection until it is toggled off, or **Streamer.bot** is restarted.

## Streamer.bot Website Integration

Decks, it's all about Decks!  With this integration, Decks can now be fully remote!  They can be opened on any browser, any device, anywhere in the world and control your **Streamer.bot** through button presses.

Under the `Integrations` tab, there is a new `Streamer.bot Website` tab, <kbd>Click</kbd> the `Settings` tab and connect to the **Streamer.bot Website**, this uses the same login mechanism that you used to sign into the website to create your Decks

Expect more things to come with this new feature!

A huge thanks to Whipstickgostop for getting the website side of things all working!

## Kofi Integration

A long asked for integration is finally here, you'll be able to react to events that come from Kofi!

Since Kofi uses WebHooks, this functionality is done through the **Streamer.bot** website, and configured there.

> This **REQUIRES** you to be connected to the Streamer.bot Website to use
{.is-info}

## Patreon Integration

You can now react to Patreon events as they happen!

Patreon also uses WebHooks, so this is done through the **Streamer.bot** website as well.

> This **REQUIRES** you to be connected to the Streamer.bot Website to use
{.is-info}

## VoiceMod Integration

With 0.1.8, you'll be able to select voices, and change options of VoiceMod from within **Streamer.bot**

The following new Sub-Actions are available:
* Get Current Voice
* Select Voice
* Select Random Voice
* Set Censor State
* Set Hear My Voice State
* Set Mute State
* Set Voice Changer State
{.grid-list}

New C# Methods available for use.

```csharp
void VoiceModSelectVoice(string voiceId);
string VoiceModGetCurrentVoice();
bool VoiceModGetHearMyselfStatus();
bool VoiceModHearMyVoiceOn();
bool VoiceModHearMyVoiceOff();
bool VoiceModGetVoiceChangerStatus();
bool VoiceModVoiceChangerOn();
bool VoiceModVoiceChangerOff();
void VoiceModCensorOn();
void VoiceModCensorOff();
```
## [Pulsoid](https://pulsoid.net/?from=streamerbot) Integration

**Streamer.bot** now has a direct integration with Pulsoid, attach an action to the Heart Rate Pulse event to receive your heart rate events.

The Heart Rate event happens every second while data is being transmitted from Pulsoid, be aware of this.

Name | Description
----:|:------------
`%measuredAt%` | Time the measurement was taken
`%heartRate%` | Heart Rate value

## HypeRate Integration

**Streamer.bot** now has a direct integration with HypeRate.io, attach an action to the Heart Rate Pulse event to receive your heart rate events.

The Heart Rate event happens every second while data is being transmitted from HypeRate, be aware of this.

Name | Description
----:|:------------
`%heartRate%` | Heart Rate value

## StreamElements

The need to find and enter your JWT token are gone.  You can now authenticate with StreamElements to give **Streamer.bot** access to your account to use features from this service.

If you were using StreamElements prior to this version, you will need to login in order to resume functionality.

## PolyPop Integration

Requires the plugin [PolyPop WebSocket Plugin](https://github.com/Jabbey92/PolyPopWebsocketPlugin/releases/tag/1.0) from Jabbey92 in order to work.

Once configured, you'll be able to trigger PolyPop alerts from within **Streamer.bot** using the PolyPop Trigger Alert sub-action

## TipeeeStream Integration
Assign an action to donations that are sent through TipeeeStream

## TreatStream Integration
Assign an action to whenever someone sends you a treat through TreatStream!

## Action Queues

A brand new tab at the top level, `Action Queues` has been added, you'll be able to find your Queues here now, instead of a drop down on the `General` tab under `Settings`.  You'll be able to add, create, delete your queues, pause them, resume them from here as well.

In addition to this, there are 2 additional tabs under `Action Queues`; `Pending Actions` and `Action History`

### Pending Actions

Here you will be able to see **Streamer.bot** working, showing you actions as they get queued up, and when they start running.

<kbd>Right clicking</kbd> on an Action will let you inspect the variables that the action was run with.

### Action History

Here you will be able to see actions that have complete, along with how long it took for them to run.

<kbd>Right clicking</kbd> on an action will bring up a context menu, letting you inspect the variables this action was run with, inspecting the variables after it was completed, as well as requeuing the action as if it was just ran.

## New Sub-Actions

### Obs Hide Scene Sources

Much like it's counter part, Obs Hide Group sources, this will hide all the sources within a scene.

### Obs Set Random Scene Source Visible

Much like it's counter part, Obs Set Random Group Source Visible, this will set a random source within a scene to visible.

### Set Voice Control Command State

Set the state of a Voice Control Command, either enable it or disable it, or toggle its current state.

### Set Voice Control Command

Set the command of a Voice Control Command to the value specified, supports parsing of values.
> This only works for Voice Control Commands that are Anywhere
{.is-info}
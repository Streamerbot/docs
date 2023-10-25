---
title: Version 0.1.5
description: 
published: true
date: 2022-09-02T03:18:34.494Z
tags: 
editor: markdown
dateCreated: 2022-06-23T02:10:32.421Z
---

# Streamer.bot v0.1.5
Released 2021-12-25{.subtitle}

*  Typos
*  Regression in Perform Command, variables were not being parsed
*  Better handling of OBS events, and issues surrounding editing
*  Better handling of OBS/SLOBS sub-actions where a scene is empty, signifying the source exists in any scene
*  Anonymous cheers could cause a crash with credits
*  Some underlying issues with Streamlabs/Streamelements sockets
*  Add error handling when importing actions, should no longer crash in the event something is malformed
*  Handle WASAPI init errors on playback, specifically if its unable to initialize the device
*  Some additional error handling in websocket server/client dialogs
*  Rare scenario where fetching mod/vip lists internally could cause a crash
*  Handle data issues with SLOBS not adhering to its on JSON structures
*  Grouping in OBS Events was not being handled properly (typo)
*  Custom WebsocketServer message event was emitting the wrong type of event internally
*  GetCredits method was putting Hype Train conductors in the wrong field
*  Twitch Slow mode sub-action was not being deserialized properly
*  Read Lines from File and Read Random Line from File sub-actions, input validation input was not working correctly
*  Creating/editing reward sub-actions when there are none could cause a potential crash
*  Fix culture parsing of decimals for streamlabs and stream elements testing of donations, decimals should work for all cultures now
*  Potential crash in some sub-actions and empty scenes
*  Drag/drop of sub-action was not properly marking cached info as dirty
*  Voice control UI was not selecting the saved input device on startup
*  Issues with Twitch dropping connection, this maybe an on going fix, trying to refine why this behaviour is happening.  This manifests as if the bot stops reacting to most Twitch actions.
*  Actions were not being flagged as dirty when using drag/drop to re-organize sub-actions, making it look like they were not being saved
*  Streamlabs donation events were being ignored, they should go through now
*  Resuming a queue should now correctly fire off any actions that were in the queue
*  Masimum values for max redeems per user/per stream are set to correct maximums now, should no longer cause a crash
*  Data type mismatch when creating Stream Markers (oops)
*  Exporting actions with a queue did not preserve is the queue was blocking
*  Importing actions did not correctly show blocking/non-blocking queue info (visual only)
*  Custom websocket server firing incorrect actions
{.changelog-fixes}

<span></span>

*  [Delay](#delay-sub-action) sub-action can now accept variables
*  Twitch Slow Mode sub-action (and C# method) has been updated to allow specifiying the delay time
*  Update [Twitch Clip C# Methods](#twitch-clip-c-methods) related methods, see section for more details
*  %s are auto removed for the variable in the LogicIf dialog
*  Add Insert and Delete as usable keys for Hot Keys and Keyboard Press
*  [Set Reward Cost](#set-reward-cost) sub-action can now accept variables, and give an operator option to add, subtract, multiply or divide the value
*  [Set Argument](#set-argument) sub-action has been updated with full parsing support for its value, and the increment option removed, see section for more details
*  New way to [pick actions](#new-way-to-pick-actions) for events!
*  Added `%rewardCost%` and `%rewardPrompt%` to the variables for reward redemptions
*  The action list in the action sub-action is now sorted alphabetically
*  Action lists returned by the HTTP server and Websocket GetActions requests are now sorted alphabetically
*  Timed Actions have been decoupled from the Twitch connection, they will now start on application start
*  Resolution for Timed Actions has been lowered to 1s from 53, this is tenetive and needs testing internally
*  Add game box art (`%gameBoxArt%` and `%oldGameBoxArt%`) to the stream update event
*  Global Get/Set sub-actions have been extended to parse the variable name, bringing support for `%variable%` parsing for the variable name itself
*  Setting auto reset first words cache time to -1 will disable this check on startup
*  Alter how commands start with check is performed, so a command of `!so` wouldn't trigger on `!socials`
{.changelog-updates}

<span></span>

*  New sub-action to set the [OBS Replay Buffer State](#obs-replay-buffer-state), as well as C# methods
*  Added 2 new [C# Methods](#obs-color-helpers) to translate colors to OBS color
*  Added a new [C# Helper Method](#obs-helper-methods) to get a connection index by name
*  New sub-action [Set Reward Title](#set-reward-title), along with a C# method
*  New sub-action [Set Reward Prompt](#set-reward-prompt), along with a C# method
*  New sub-action [Update Reward](#update-reward), where you can set the title, prompt and cost of a reward in one call, along with a C# method
*  Added ability to double click to edit Websocket Servers and Clients
*  Added new variable `%spokenTextInput%` to Speech To Text events for Commands, this is the text spoken without the trigger word, and is only support for Start based commands
*  Added new variable `%spokenCommand%` to Speech to Text events that will contain the command that triggered the event
*  A new Twitch scope will be requested on first start, Commercial Edit
*  New sub-action [OBS Get Scene Item Properties](#obs-get-scene-item-properties) to get the properties of a scene item, as well as a C# method
*  New sub-action [Start Commercial](#start-commercial) to start commercials on your channel, as well as C# methods
*  New sub-action [OBS Set Media Source File](#obs-set-media-source-file) to set the file of an OBS Media Source, as well as C# methods
*  New sub-action [OBS Set Image Source File](#obs-set-image-source-file) to set the file of an OBS Image Source, as well as C# methods
*  Support for [DonorDrive](#donordrive) services! This includes ExtraLife, StackUp and any other charity drives that use DonorDrive.
*  The first [Inline Function](#inline-function) has arrived!
*  Added new keys to [Hot Keys and Keyboard Presses](#new-hot-keys-and-keyboard-presses)
*  Add new [C# Methods](#command-cooldown-methods) to alter the cooldowns of a command
*  New sub-action [Get Commands](#get-commands) to get a list of your commands
*  New sub-action [Run Commercial](#run-commercial) to run a commercial on your channel, as well as a C# method
*  Added option to Gift Subs to ignore those that come from a Gift Bomb, there is also a variable `%fromGiftBomb%` that can be checked
*  With the new way actions are selected, most lists have a new menu item to select the action without needing to edit
*  The user list in the Timeout User sub-action is now sorted alphabetically, and I've updated the control to support auto complete suggestions to help find user names.
*  New sub-action [Get Command State](#get-command-state) to get the state of a command, or command group
*  New sub-action [Get Action State](#get-action-state) to get the state of an action, or action group
*  Added some [new action wide variables](#new-action-wide-variables)
*  New sub-action [TwitchSpeaker Speak](#twitchspeaker-speak) to provide a simpler way to get TwitchSpeaker to speak for you, as well as a C# method
*  3 new Twitch events can be broadcast across the websocket, message deletion, user timeout and user ban
*  New sub-action **Break** that will halt the action from continuing, mostly used when debugging
*  Added new events for twitch message deletion, user being timed out, and a user being banned
{.changelog-new}

## DonorDrive

You can add either your team, or personal campaign for ExtraLife, StackUp or any other charity that uses DonorDrive, and attach an action to a donation event.

This is not limited to just 1, you can add multiple as well.

More info to be filled in.

## Inline Function

Up until now, the only thing that could be parsed were `%variables%`, I have finally added the first function to this, `$math()$`.

Anywhere there is full parsing, you can now perform math operations, and also use variable within the math function itself.

Here is just a simple example of an action:
* Set Argument `%x%` to `1`, `%x%` is now 1
* Set Argument `%x%` to `$math(%x%+1)$`, incrememnt `%x%` by `1`, `%x%` is now `2`
* Set Argument `%x%` to `$math(%x%^2)$`, set `%x%` to `%x%` to the power of `2`, `%x%` is now `4`
* Set Argument `%x%` to `$math(%x%*16)$`, set `%x%` to `%x%` times `16`, `%x%` is now `64`

A page with the possible usages of the `math` function will be added as well, as it is more then just your basic arithmetic (yes, you can even do derivatives or integrals if you wanted to).

## New Way to Pick Actions

With this update, I've completely removed the mess of dropdowns to select events.  This was slowing down the application with the amount of updates this could generate to keep track of any changes to your actions.

There is now a clickable button that will bring up a dialog with your actions grouped and sorted like they are on the main actions page.  This dialog is very much a WIP, and will evolve over time.

In addition to events, most dialogs where you picked actions (Commands, Channel Reward, Timed Actions, etc) have also received this update.

As an added bonus, most of the lists where you edit these kinds events, now have a new context menu item to be able to change the action without having to go in and edit the command, reward, etc.

## Set Argument

With the addition of the `$math()$` inline function, the **Set Argument** sub-action has been updated to fully support parsing its value, and the Increment option has been removed, as you can now use the math function to do this.

![sub-action-set-argument-002.png](/sub-action-set-argument-002.png)

> A configuration upgrade will happen, converting any Set Argument that is flagged as increment will have its value converted to `$math(Variable+Value)$`, there is the possibility this may not fully work, so it is advised to check any Set Arguments you have that were converted.
{.is-info}

## New Hot Keys and Keyboard Presses

A few new keys were added to be the list of keys usable for Hot Keys and Keyboard Press

* Semi Colon `;:`
* Forward Slash `/?`
* Tilde `~`
* Opening Square Brace `[{`
* Backslash `\|`
* Closing Square Brace `]}`
* Double Quote `"`
* Comma `,<`
* Minus Sign `-_`
* Period `.>`
* Plus Sign `+=`
* Break
* Scroll Lock
* Media Next Track
* Media Previous Track
* Media Stop
* Media Play/Pause
* Media Volume Mute
* Media Volume Down
* Media Volume Up

## Twitch Clip C# Methods

Previously, the C# calls to get Twitch clips, only allowed getting all the clips, leaving it upto you to sort through them afterwards.  If there were many clips for a user, this could take a while to fetch, and as it wsa a paginated call, it was only grabbing 20 at a time leading to further slow down.

The first fix, it now fetches 100 at a time (the maximum allowed per call),  This means, ever paged call takes approximately 800 milliseconds to complete.

The methods for fetching clips have been updated to allow for a count to be specified, and it will only grab that many clips for a user, default sorted newest to oldest.

They have also been updated to specific a date range (start and end date) to look for clips, as well as a day timespan, to specifiy the past 7 days, or the past 30 days, etc.

```csharp
List<ClipData> GetClipsForUser(int userId, int count);
List<ClipData> GetClipsForUser(int userId, DateTime start, DateTime end);
List<ClipData> GetClipsForUser(int userId, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForUser(int userId, TimeSpan duration);
List<ClipData> GetClipsForUser(int userId, TimeSpan duration, int count);
List<ClipData> GetClipsForUser(string userName, int count);
List<ClipData> GetClipsForUser(string username, DateTime start, DateTime end);
List<ClipData> GetClipsForUser(string username, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForUser(string username, TimeSpan duration);
List<ClipData> GetClipsForUser(string username, TimeSpan duration, int count);
List<ClipData> GetClipsForGame(int gameId, int count);
List<ClipData> GetClipsForGame(int gameId, DateTime start, DateTime end);
List<ClipData> GetClipsForGame(int gameId, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForGame(int gameId, TimeSpan duration);
List<ClipData> GetClipsForGame(int gameId, TimeSpan duration, int count);
```

## New Action Wide Variables

If Twitch is connected, actions will have the following five variables available to them

Name | Description
----:|:------------
| `%broadcastUser%` | The Twitch display name of the broadcast account |
| `%broadcastUserName%` | The Twitch user name of the broadcast account |
| `%broadcastUserId%` | The Twitch user ID of the broadcast account |
| `%broadcastIsAffiliate%` | true/false value indicating if the broadcast account is an affiliate |
| `%broadcastIsPartner%` | true/false value indicating if the broadcast account is a partner |

## New Sub-Actions

### Set Reward Title

Change the Title of an existing reward, this also supports the use of `%variables%`

![sub-action-set-reward-title-001.png](/sub-action-set-reward-title-001.png)

#### New C# Method

```csharp
void UpdateRewardTitle(string rewardId, string title);
```

### Set Reward Prompt

Change the prompt of a reward, this also supports the use of `%variables%`

![sub-action-set-reward-prompt-001.png](/sub-action-set-reward-prompt-001.png)

> There is a bug on Twitch's side with the API call, it is not possible to set the prompt to an empty value once it has been set.  This issue also happens with Twitch's own editing of a reward on the website
{.is-info}

#### New C# Method
```csharp
void UpdateRewardPrompt(string rewardId, string prompt);
```

### Update Reward

Change the title, prompt and/or cost of a reward in 1 sub-action.

![sub-action-reward-update-001.png](/sub-action-reward-update-001.png)

#### New C# Method
```csharp
void UpdateReward(string rewardId, string title = null, string prompt = null, int? cost = null);
```

### OBS Replay Buffer State

New sub-action to control the Replay Buffer state, no longer need to use OBS Raw to achieve this

![sub-action-obs-set-replay-buffer-state-001.png](/sub-action-obs-set-replay-buffer-state-001.png)

#### New C# Methods for OBS Replay Buffer State
```csharp
void ObsSetReplayBufferState(int state, int connection = 0);
void ObsReplayBufferStart(int connection = 0);
void ObsReplayBufferStop(int connection = 0);
void ObsReplayBufferSave(int connection = 0);
```

### OBS Get Scene Item Properties

New sub-action that will make a `GetSceneItemProperties` call to the websocket, and much like OBS Raw, will add the results into your arguments in the form of `props.<path>`

#### New C# Methods for OBS Get Scene Item Properties
```csharp
string ObsGetSceneItemProperties(string scene, string source, int connection = 0);
```

### Run Commercial

Allows you to start a commercial on your channel.  Commercials can be either 30s, 60s, 90s, 120s, 150s, or 180s in duration.

![sub-action-run-commercial-001.png](/sub-action-run-commercial-001.png)

#### New C# Method

```csharp
void TwitchRunCommercial(int duration);
```

### OBS Set Media Source File

Allows you to change the file of an OBS Media source, `%variables%` are supported.

![sub-action-obs-set-media-source-file-001.png](/sub-action-obs-set-media-source-file-001.png)

#### New C# Method
```csharp
void ObsSetMediaSourceFile(string scene, string source, string file, int connection = 0);
```

### OBS Set Image Source File

Allows you to change the file of an OBS Image source, `%variables%` are supported.

![sub-action-obs-set-image-source-file-001.png](/sub-action-obs-set-image-source-file-001.png)

#### New C# Method
```csharp
void ObsSetImageSourceFile(string scene, string source, string file, int connection = 0);
```

### Get Commands

Will give you a list of your commands, into the variable of your choice.  Can be limited down by command group, or if the user doing the command has permissions

![sub-action-get-commands-001.png](/sub-action-get-commands-001.png)

2 variables will be added, the first will be a comma delimited string of your commands, that will be placed in the variable you picked, as well, a list of the commands (for use in C#) will be placed in `[VariableName]List`, so from the screenshot, `%commandsList%` would contain a `List<string>` of your commands

### Get Command State

Using this sub-action you can get the state of a command, whether its enabled or disabled, as well as get the state of a group of commands, if they're all enabled or disabled, or mixed.

#### Variables provided for `Get Command State`

Name | Description
----:|:------------
| `%commandState%` | The state of the command `true`/`false` |

#### Variable provided for `Get Command Group State`

Name | Description
----:|:------------
| `%commandGroupState%` | The state of the command group, see table below for information |
| `%commandsEnabled%` | A `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are enabled |
| `%commandsDisabled%` | A `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are disabled |

#### Possible values for `%commandGroupState%`

| Value | Description |
|   ---:|-------------|
| `0` | All disabled |
| `1` | All enabled |
| `2` | Mixed |

### Get Action State

Using this sub-action you can get the state of an action, whether its enabled or disabled, as well as get the state of a group of actions, if they're all enabled or disabled, or mixed.

#### Variables provided for `Get Action State`

Name | Description
----:|:------------
| `%actionState%` | The state of the action `true`/`false` |

#### Variables provided for `Get Action Group State`

Name | Description
----:|:------------
| `%actionGroupState%` | The state of the command group, see table below for information |
| `%actionsEnabled%` | A list of action IDs that are enabled |
| `%actionsDisabled%` | A list of action IDs that are disabled |

#### Possible values for `%actionGroupState%`

| Value | Description |
|   ---:|-------------|
| `0` | All disabled |
| `1` | All enabled |
| `2` | Mixed |

### TwitchSpeaker Speak

To simplify uusing TwitchSpeaker with **Streamer.bot**, you can us this sub-action to have messages spoken by TwitchSpeaker.  Before you'd have to use the UDP broadcast sub-action.

#### New C# Method
```csharp
void TtsSpeak(string voiceAlias, string message, bool badWordFilter = false);
```

> This requires you to be using TwitchSpeaker for TTS
{.is-info}

## New C# Methods
### OBS Color Helpers
```csharp
long ObsConvertRgb(int a, int r, int g, int b);
long ObsConvertColorHex(string colorHex);
```

### OBS Helper Methods
```csharp
int ObsGetConnectionByName(string name);
```

### Command Cooldown Methods
> The ID can be retreived by right clicking a command, and clicking the Copy Command ID option
{.is-info}

```csharp
void CommandResetGlobalCooldown(string id);
void CommandAddToGlobalCooldown(string id, int seconds);
void CommandResetUserCooldown(string id, int userId);
void CommandAddToUserCooldown(string id, int userId, int seconds);
void CommandResetAllUserCooldowns(string id);
void CommandAddToAllUserCooldowns(string id, int seconds);
```
---
title: Version 0.1.4
description: 
published: true
date: 2022-09-02T03:17:39.662Z
tags: 
editor: markdown
dateCreated: 2022-06-23T02:09:12.646Z
---

# Streamer.bot v0.1.4
Released 2021/10/23{.subtitle}

*  Various typos
*  Editing a channel reward and setting max per stream works correctly now
*  Creating or duplicating a channel reward correctly says its owned now
*  Add Follow Age Info was not allowing variable entry
*  Streaming with no game category selected would cause a crash
*  Community Goal contribution event was tied to the wrong underlying event
*  Added a flag to testing the follow event, so it can bypass the built in follow/unfollow protection
*  Potential crash when a websocket or http server port was in use
*  Harden some of the code surrounding Twitch tokens, hopefully less crashes
*  Community goal percent completed calculation was wrong
*  Enabling/disabling commands by group was not correctly working
*  Re-enable maximize box on main window
*  Poll update and complete events were executing the wrong action setting
*  The Twitch Raid start event sends the profile image url at 70x70, updated this to be the larger 300x300
*  PlaySound/PlaySoundFromFolder C# methods were not properly waiting for sound to complete
*  Handle potential crash on startup related to voice control
*  Was not correctly forgetting bot account
*  Poll/Prediction Create, Update and Complete actions were being stored but not shown, the visual bug has been fixed.
*  Find Refs in C# Execute could cause a crash if there is a bad image (a dll) in your application folder
*  Some hardening of code surrounding export to clipboard
*  SetTimerState sub-action not resetting the timer correctly when enabling
*  StreamElements/Streamlabs events no longer try to resolve the user to a seen viewer
*  Community goal help text
*  S potential deadlock that could occur with OBS Websockets
*  Setting a source's mute state in SLOBS should work correctly now
{.changelog-fixes}

<span></span>

*  Credits no longer include the Broadcaster or Bot account in any lists
*  [Perform Command](#perform-command) sub-action is being updated with new options and capabilities
*  [ReadLinesFromFile](#readlinesfromfile-and-readrandomlinesfromfile) and [ReadRandomLinesFromFile](#readlinesfromfile-and-readrandomlinesfromfile) were updated to parse variables, and attempt auto-typing
*  Added `%obsRaw._json%` variable to the OBS Raw sub-action, it contains the result as is, so it could be parsed in a C# action
*  Missed some variables in [Twitch Prediction](#twitch-predictions) completion event
*  Missed some variables in [Twitch Polls](#twitch-polls) completeion event
*  [Commands](#commands) got a bit of an overhaul, check the section for more details
*  When adding actions, group will be auto filled based on selection
*  Improved shutdown time
*  Change how [Twitch Gift Sub Bombs/Gift Subs](#twitch-gift-sub-bombgift-subs) are handled
*  OBS Set Source Filter State sub-action will now list the global audio sources if they are in use, and will be shown in the list before the scene sources
*  When switching scenes in most OBS sub-actions, an attempt will be made to pre-select the same named source if possible, this is an ongoing update
*  Variable replacements now supports inline formatting, using any of the standard C# formatting options, example `%donatedValue:N2%` would give a number with 2 decimal places, if the value is a number
*  Set Argument subaction can now accept variables as values, be sure to use %s, so you can assign a variable to another variable
*  Logic If now supports variable names as comparison values, be sure to use %s
*  UDP Broadcast sub-action now behaves similarly to OBS Raw in how replacements are done, invalid characters should no longer be an issue, and numbers will be treated as numbers
*  Add new `%messageCheermotesStripped%` variable to a cheer event, that retains all the emotes, and only stiprs cheermotes
*  Allow variable usage for SLOBS Set Active Scene sub-action
*  Made the text entry for the Twitch Send Message sub-action a bit biger and wrap lines, so more can be seen
{.changelog-updates}

<span></span>

*  New [Hot Key Support](#hot-key-support)
*  [Confirimation dialog](#confirmation-dialogs) when deleting an action, a sub-action, or all sub-actions
*  [Confirimation dialog] when closing bot.
*  Minimize/Close to tray option
*  Expanded OBS capability with [OBS Events](#obs-events) being able to trigger actions
*  New [OBS Take Screenshot](#obs-take-screenshot) sub-action
*  New [OBS Set Audio Track State](#obs-set-audio-track-state) sub-action
*  New [OBS Set Media State](#obs-set-media-state) sub-action
*  New [Twitch Set Channel Title](#twitch-set-channel-title) sub-action
*  New [Twitch Set Game](#twitch-set-game) sub-action
*  Add ability to enable/disable all actions in a group from context menu
*  Block port 4444 from being used for **Streamer.bot's** own internal websocket server
*  Introduced a new option for commands, [Command Cooldown Action](#command-cooldown-action), check for more details
*  You can now drag sub-actions around to move them **this is still a bit experimental and might have some issues**
*  Ogg Vorbis is now a supported playback format for sound files
*  Commands now have a **Case Sensitive** option
*  Added C# methods for creating [Twitch Predictions](#twitch-predictions)
*  Add C# methods to enable/disable [Commands](#commands)
*  Added 2 new variables, `%createdAt%` and `%accountAge%` to the Get Target Info sub-action, accountAge will be given in seconds
*  Update [Twitch Polls](#twitch-polls) to be able to handle the `/endpoll` command (Poll Terminated action)
*  Add option to export actions to file
*  Add indicator to exporting to clipboard that it was successful
*  Add new context menu item when right clicking a user to perform some twitch actions, at the moment, just banning and adding/removing mod/vip status
*  New Set Command Group State sub-action
*  New Set Action Group State sub-action
*  Quote settings now shows all your quotes, and can be deleted, this is just the start of UI for quotes
*  Add ability to duplicate a group and all of it's sub-actions
*  When connecting to Twitch, your list of mods and vips are updated automatically
*  [Experimental Linux Support](#experimental-linux-support) **READ THIS SECTION FOR IMPORTANT INFORMATION**
*  Add new sub-action for enabling/disabling slow mode in your twitch channel
*  Add new sub-action for creating a clip, as well as a C# method. **NOTE, There is no control over the clip created, title, length, etc**
*  Add new sub-action for creating a stream marker, as well as a C# method; you can provide a description for the marker
* **Misc:** Update some libraries that are used
{.changelog-new}

<span></span>

## Hot Key Support
After much requesting, it's here, Global Hot Key support!  There is also a new sub-action to send keyboard presses! 

The keys you can use for creating a global hotkey are currently limited to keys that make sense, and can always be expanded.

The sub-action for keyboard presses, at the moment, is really meant for pressing global hot keys, and may evolve over time to be able to specify a specific window/application.

![sub-action-keyboard-press.png](/sub-action-keyboard-press.png)

## Perform Command
The **Perform Command** sub-action has had a bit of an overhaul to give you more options in setting up to run a command.

![sub-action-perform-command.01.png](/sub-action-perform-command.01.png)

The new additions allow you to set the working directory, the arguments to use (which supports variable replacement), as well as being able to set environment variables (also supporting variable replacement).

**Note:** *There was a bug in the old version where it could not run commands with arguments properly.*

For example, the following could be used for executing a python script.

| Property | Value |
|      ---:|-------|
| Command | `C:\Python27\pythonw.exe` |
| Working Directory | `C:\StreamStuff` |
| Arguments | `C:\StreamStuff\sub-printer.py` |

Environment Variables could be:

| Key | Value |
| ---:|-------|
| `USER` | `%user%` |
| `TIER` | `%tier%` |
| `MESSAGE` | `%message%` |

## ReadLinesFromFile and ReadRandomLinesFromFile
Read Line From sub-actions have options to now parse variables in the line read, and to auto-type instead of always adding as a string

![sub-action-readlinesfromfile-01.png](/sub-action-readlinesfromfile-01.png)

![sub-action-readrandomlinefromfile-01.png](/sub-action-readrandomlinefromfile-01.png)

## OBS Events
New with this version, you can now assign triggers to events that OBS transmits across the websocket connection.

![obs-events-01.png](/obs-events-01.png)

The data that an event emits, is added onto the arguents the same way it is with results from `OBS Raw`, as well as a `%obsEvent._json%` variable that can be parsed in C# (`JObject.Parse()`) for easier use.

OBS events are per-connection based.

## Confirmation Dialogs
When closing **Streamer.bot** you'll be prompted if you're sure you want to close, with the option of not asking again.

![close-prompt.png](/close-prompt.png)

When you delete an action, or a sub-action, you will be prompted to confirm the deletion, with the option of not asking again.

![delete-confirm.png](/delete-confirm.png)

You can reset these confirmations under the `User Interface` tab in `Settings`

## Twitch Predictions
Seems I missed adding in some variables to the completion event, unlike polls where a winner is determined by a fixed vote, predictions are resolved, and the broadcaster or a moderator pick the specific winner.

In addition, I added a `%prediction._json%` argument, which contains a JSON string of the event that can be parsed in C# (`JObject.Parse()`) for easier use.

| Value | Description |
|   ---:|-------------|
| `%prediction.winningIndex%` | Either a 0 or 1 depending on which outcome was chosen as the winner |
| `%prediction.winningOutcome.id%` | The ID of the winning outcome |
| `%prediction.winningOutcome.title%` | The title of the winning outcome |
| `%prediction.winningOutcome.users%` | How many users voted for this prediction |
| `%prediction.winningOutcome.points%` | The total number of channel points used by users |
| `%prediction.winningOutcome.color%` | The colour of the winning outcome |

### Prediction C# Methods
There are 4 new C# methods that can be used to create a prediction from C# code.

```csharp
string TwitchPredictionCreate(string title, string firstOption, string secondOption, int duration);
void TwitchPredictionCancel(string predictionId);
void TwitchPredictionLock(string predictionId);
void TwitchPredictionResolve(string predictionId, string winningId);
```

## Twitch Polls
Even tho a poll can technically end in a tie, I added the winning choice information into the arguments.

In addition, I added a `%poll._json%` argument, which contains a JSON string of the event that can be parsed in C# (`JObject.Parse()`) for easier use.

| Value | Description |
|   ---:|-------------|
| `%poll.winningIndex%` | The index of the winning choice, from 0 to 4 |
| `%poll.winningChoice.id%` | The ID of the winning choice |
| `%poll.winningChoice.title%` | The title of the winning choice |
| `%poll.winningChoice.votes%` | Number of regular votes |
| `%poll.winningChoice.bitVotes%` | Number of bit based votes |
| `%poll.winningChoice.rewardVotes%` | Number of channel point based votes |
| `%poll.winningChoice.totalVotes%` | Total number of votes for the choice |

### New Action
When using `/endpoll` in your chat to stop an active poll, its sent through as terminated, not completed; a new assignable action to the terminated event has been added.

## Commands
After seeing and hearing the feedback, commands got a bit of an overhaul.

To start with, something simple, when you add a new command, if you happened to right click on an existing command and picked add, the new command will be auto-set to the group of the selected command.  Right clicking add while on a group line itself, will also auto assign the group when adding a command.

You can now have multiple "commands" for a single command, also, Regex based input is supported.

> Regex comparisons can be heavy; even with the precompilations that exist for C#, they can become slow if the expression itself is not optimized.  There are no limits on how many you can create, but just be aware, every message that comes through is checked against all commands to see if any should be run.
{.is-warning}

The introduction of regex, is just simple at the moment, and may get a bit more complex afterwards (for example, regex capture groups being added as arguments)

One other thing to note, the `%rawInput%` variable for commands, specificially the **Start** location, auto strips the command from the start, at the moment, with a regex based command, it will behave like **Anywhere** and not remove the matched section(s), I may alter this slightly and add a 2nd variable that gives you both, one with, and one without, I'm unsure yet.

![commands-multi-01.png](/commands-multi-01.png)

![commands-regex-01.png](/commands-regex-01.png)

### Command C# Methods
Two new C# methods were added to be able to enable/disable a command.  Unlike other methods that only need a title, this requires the ID of the command, this can be retreived by right clicking on a command and selecting `Copy Command Id`

```csharp
void EnableCommand(string id);
void DisableCommand(string id);
```

## Command Cooldown Action
From the suggestion board, letting a user know that a command was on cooldown was requested, and instead of just hard coding this, I've added this as a configurable action instead.

A cooldown action can only trigger from a command that has a location of `Start` or `Exact`, regex based commands, or anywhere location will not trigger this action, even if it is on cooldown.

Also, only a `Message`, `Subscription` and `ReSubscription` can trigger a cooldown action.

There is a new column in the `Commands` list that shows the `Cooldown Action` associated with a command.

Available variables:

| Value | Description |
|   ---:|-------------|
| `%command%` | The command that was used |
| `%cooldownLeft%` | How many seconds are left for the cooldown, and is the maximum of the global and user cooldown left |
| `%globalCooldownLeft%` | How many seconds are left for the global cooldown of the command |
| `%userCooldownLeft%` | How many seconds are left for the user cooldown of the command |

There is also a new websocket event that can be subscribed to, `CooldownEvent` for `Commands`

![sub-action-commandcooldown-01.png](/sub-action-commandcooldown-01.png)

The most basic subaction you could add, would be a `Twitch Message` with the message `%user%, %command% is on cooldown for %cooldownLeft%s`

## Twitch Gift Sub Bomb/Gift Subs
In previous versions, when someone dropped a gift bomb (more then 2 gift subs in a single go), only the gift bomb event itself was triggered, and all associated gift sub events for it were silently discarded.

With this version, the gift subs are no longer discarded, they are now also sent, and there is an argument `%fromGiftBomb%` that will exist. If this is true, the sub is from a gift bomb, if false, its not.

I've also added `%subBombCount%` which will give the number of gift subs, if ths gift sub belongs to a gift bomb.

One last new argument is `%cumulativeMonths%`, this can have how many months the user receiving the gift sub has been subscribed for, if its 1, they are a new subscription, if its > 1, then its a resub.  There are chances where it can be 0 from what I've seen.  So this value could be used to welcome a new gifted subscriber.

## New Sub-Actions

### OBS Take Screenshot
Up until now, you had to use OBS Raw to take a screenshot in OBS, here is a sub-action ot make things a bit simpler.

![sub-action-obs-takescreenshot-01.png](/sub-action-obs-takescreenshot-01.png)

`Scene`, `Source` and `File Path` all support variable replacements, and after a screenshot is successfully taken, the full file path is added back onto the arguments as `%screenshotFile%`.

There is a new date time friendly variable that can be used, `%filedatetime%` which is of the format `yyyyMMdd.hhmmss`.

### OBS Set Audio Track State
With this sub-action you can alter which audio tracks a source can be active on

![sub-action-setaudiotrackstate-01.png](/sub-action-setaudiotrackstate-01.png)

> This sub-action ***requires*** obs-websocket version 4.9.1
{.is-info}

## OBS Set Media State
Control the state of media playback, you'll be able to `Play`, `Pause`, `Restart`, `Stop`, `Next`, `Previous` the specified media.

![sub-action-obs-setmediastate-01.png](/sub-action-obs-setmediastate-01.png)

The following C# methods were also added to control media via code.
```csharp
void ObsSetMediaState(string scene, string source, int state, int connection = 0);
void ObsMediaPlay(string scene, string source, int connection = 0);
void ObsMediaPause(string scene, string source, int connection = 0);
void ObsMediaRestart(string scene, string source, int connection = 0);
void ObsMediaStop(string scene, string source, int connection = 0);
void ObsMediaNext(string scene, string source, int connection = 0);
void ObsMediaPrevious(string scene, string source, int connection = 0);
```

## Twitch Set Channel Title
Using this sub-action, you'll be able to set the title of your channel, either to a fixed value, or using variables.

![sub-action-setchanneltitle-01.png](/sub-action-setchanneltitle-01.png)

The following C# method was also added to set your channel title via code.
```csharp
bool SetChannelTitle(string title);
```

An example action that you can assign to a `!title` command
```
TlM0RR+LCAAAAAAABACVVNmOm0gUfR9p/sGylLdgUSx2EykP3XTbhlYzwhuYoR9qA9MulrDYjaP8+xQQp7GtaBQsC7jn1rnnnuLW97//GgyGB5oXUZoMvwzA5zaQwJjyt+GSlvoOJgllq6hkdNihEJc8u+AJ/zbvg8H37sahiDTLFBWiAMhjQUUTRVDGgAp36hgKqiJTWVEIgEDuuNpF3ypaNeWSirGPKE0gYrThK/OKfsR72gY/xQ166tqcME+rrEny+NWLQ3aEdbGomlYDyIoebQ4Tksb3bWu3KE4TXOU5Tcpb7MaOC0valLLVx/V8yuHRSLKq/PShqmecLGp3QFMlYUwJERQZEgGKARYoVUQJUDIZg/HVwiONwl2jShyJl0hZZ01NoF6Gz95cuN1pSAh9b5g+oj8+/66l3jasDN7dghYVK6/EEVrgPMp+ejq8QveUZvcsOtAbT7sdoQHljmN6ZW0L6l983+GC02Ph+y8RztMiDcqR9bTy/WnOtR3TfO/7B2UkjmRRBprvxwVOcxahEWFs2Kd7vayL6pLqKWm7I66VoRiHa5mdyGxT/nMUnx/t7Egcs4DOS7iV3ndYfglt8GAsHZXHVMbxyaOdmni+idCMvRkz84CkY7hwd2wrb0RvGWYNTjmXbjNp6xohljdvW2lzwvW9ZjxZB5R4DCd2tZlpOpK0wnOm1fNsWnuyhYxkkZHZO1v/WmOS51Vh6eHeJPG0Nubmjois4vVF41EMt66ZYFBEOJ7KXOORuHbkLtU1ApaIY1Z5dZh1faWm7rDY0Hcn4lhvnmudnu1WY9sPvz+un8JqLW0q7wkwLFs7T1pzwFxDd1F4y4eT59ohmd2NjXlZb11iouQBkLkYnfUFHR9Dc4u1nG4X19eWvdTVleeo+5XDe5KmCfdpb7BNteVec24R1Wd+JqLZ+v9q1J67ADhWQjI3gddiTON7w//p16svMcspTuMsYr/5FAllsF6WML8d/970KjggGgKqcKdNVEGZUFFAeAIETCkKAsB/WPrT6dWa608HGPQG+Pz4en1gzRqadrRe++ccYzArKOmhHdgSdZndgX0Gf/wHhK9EBUQGAAA=
```

## Twitch Set Game
Using this sub-action, you'll be able to set the game for your channel, again using a fixed game that you can set from a list, or by using variables

![sub-action-setchannelgame-01.png](/sub-action-setchannelgame-01.png)

![sub-action-setchannelgame-02.png](/sub-action-setchannelgame-02.png)

The following C# methods were also added to set a game via code.
```csharp
GameInfo SetChannelGame(string game);
bool SetChannelGameById(string gameId);

public class GameInfo
{
		public int Id { get; set; }
		public string Name { get; set; }
		public string BoxArtUrl { get; set; }
}
```

An example aciton that you can assign to a `!game` command
```
TlM0RR+LCAAAAAAABACVVctu2kAU3VfqPyCk7mLkJ+DughPATuMUiG1wncW8MA7jR/2Amqr/3hkbBAF1UUsI5p65Z84913f4/flTp9PdkbyI0qT7tSPdNYEExIStugtSGhuQJIROeKQFASrZ5oLhP/i60/ndfjEowjwLA62P4AALfayqgirJQwGA/oAt+0ofaiKBUr/lapJ+VqTipyUVpecoSQCkhPOVeUXO8QtpnaO2zllcsyXM0yrje3z2XMQB3YO6mFe80DWgxQVrDhKcxvdNZbcoShNU5TlJylvsxo0PjjRbirTKERct3n2Ih8dSvuRgbyZZVX7p3m4wG0uvgNZnoKqqBpW1oANREVQVi4KuKKIwJAoZAl0fDofSVeKeROGGVyH2rsSUdcbFSP0rCUcvPzSn1ZBg8osznaN/7v5lwUXXeLPmpKhoeaUNkwLlUXZswXXJW0KyexrtyE0L2gaSNWENQuSqEw1ofA0Cj+lN90UQPEcoT4t0Xfbsx9cgGOdMzz7Nt0GwU3tiTxEVSQ+CuEBpTiPYw5R2L+nePp4L65IYKW6Kw0s7gzEKHYUe8MQtX/bi08Ms22PPKoD3HK7kXxukPIczaWQuPI3FNMrwwcMstdDUjeCEvpsTawflfThfbuhKcUV/EWYcJ4zLmFF5tTRDpLjvK9k9oPpeNx/tHUx8ipJZ5U50A8p64Xvj6mkyrn3FhmaMN9BzX7Fnv/tL+2BSMWt1pZbh0dg0NocT9jRrzmj0nM7y5XHpOxrjcMLvi9EGxfjg1Vay8iT6GjNsYeFvdL5zlHnN6kmejO0p/8F5DCtHdiv/UaJIsTe+7DDAmvJcc2pTbIxEeEhDIjcaX3h8vTAbfSxfbzW6BZId2wi3Rw+2Fo7HtTm1NlikFfNNNB/EcLW0EiQVEYrHCvN2j5ezaLnQHCjZIopp5dfhkXdrcf+/UZvCeG7zulcepgyIXE/LYawrMBo19b1Eo8GZb66b0bG2pdjoQbEr4qVVmdN5jT2nwdbMQ/65enuznKA0ziL6j9cXEwrqRQny2xvmYuA1fYg0HSCBQCIKKh6obODVgbCWIegrcA36ZPC/A6/z539nXrqY+dPPt+s7ccJpmnF8u7xKKQVZQfAF2oINUbuz/Us4gX/+AqlLhx2lBgAA
```

## Experimental Linux Support

> There is no guarentee this will work 100%, there are areas of the app that may not function correctly, so this will be a complete work in progress depending on time/effort.
{.is-warning}

It is possible to run this current version (**0.1.4**) using wine/wine64 within Linux

The entire network stack was re-written to make this possible, as it was a major blocker.

I've been doing some tests using the staging version of Wine, which is v6.19 in Ubuntu 20.04 LTS.

For your Wine setup, you'll want the following:
```
winetricks dotnet472
winetricks d3dcompiler_47
winetricks dxvk
```
You will also want to make sure gnutls (for 32-bit, lib32-gnutls).

This information should also apply to TwitchSpeaker, one area that will not work in TwitchSpeaker are SAPI5 voices, and the Azure voices may also not work. Again, this is very experimental.

A dedicated page on the wiki will likely be created for those who are using/testing it under Linux to list what works and what the current issues are.

> Running **Streamer.bot** and/or **TwitchSpeaker** under Linux is considered to be experimental, so expect bugs/issues.
{.is-warning}
---
title: Version 0.1.3
description: 
published: true
date: 2022-09-02T03:23:31.340Z
tags: 
editor: markdown
dateCreated: 2022-06-23T02:08:17.858Z
---

* Logic if sub-action for does exist, code path was unreachable
* Importing actions which contained OBS actions, was not correctly defaulting to first configured OBS instance
* Importing actions which contained ClearActionQueue and SetActionQueuePauseState
* ClearActionQueue and SetActionQueuePauseState to handle if an invalid queue has been selected
* Pyramids, a change to the way emotes were handled broke this feature
* Stream Update could cause a crash if your category was empty, On Connect was enabled, and at least 1 Game action was configured 
* Typo in the Gift Bomb event, was `totalGits`, should have been `totalGifts`
* Assigning an action to a group using the context menu no longer causes all groups to expand
* Hosting event had the potential to cause a crash
* Clicking cancel when creating a poll will no longer warn that poll could not be created
* OBS Raw variable replacement tries to be type aware, if the variable is a number, it won't put it in quotes for instance
* Possible crash when removing/updating a speech to text command when its not actively running
* Play Sound From Subfolder sub-action was setting the folder properly when editing
* Get Random Number sub-action was not linked to the correct edit action (whoops?)
* Quote messages were not being sent over bot account if it was connected, this will probably change to actions in another release for better control
* If the logic if sub-action was not set to run immediately, it would not break if the after action was set to this
* Misc fixes/tweaks that are probably forgotten
{.changelog-fixes}

<span></span>

* As per a few suggestions, the **Speech To Text** tab has been renamed to **Voice Control**
* First pass over the **[Groups](#groups)** section has started
* Execute C# Code [Find Refs](#find-refs) has been updated a bit, and is a lil more forgiving when it tries to add the needed references
{.changelog-updates}

<span></span>

* The Rewards -> Configure Rewards sub-action has been updated a bit, window is now resizeable and added a context menu for moving rewards as well
* Mask the Streamlabs and StreamElements tokens, with a show/hide button
* Added [Subscriber](#subscriber-only) and [Emote](#emote-only) Only Sub-Actions
* Added Subscriber and Emote Only methods for Execute C# Code
* Added new Sub-Action [Read Lines From File](#read-lines-from-file)
* Channel rewards are now groupable, and sortable by `Name`, `Cost` and `Owned` within there groups
* Added ability to enable/disable/pause/unpause all owned rewards in a group through context menu
* Added ability to enable/disable all commands in a group through context menu
* Added [Fetch Url](#fetch-url) sub-action
* Added [Pick Color](#pick-color) sub-action
* Copy pasta sub-actions!  Be sure to [read below](#copy-pasta-sub-actions) for specifics
* Added a [Comment](#comment) sub-action
{.changelog-new}

## Copy Pasta Sub-Actions
As more of a QoL improvement, I have started implementing some basic copy and paste functionality.  First up to get this capability is the sub-actions.

While it does copy data to your clipboard, meaning it could be shared; it is **not** recommended to, currently, when you paste an action, no real sanitization and checks are done (*yet*), as it is meant to be pasted back into your own running instance of **Streamer.bot** which has all the supported components setup already (i.e., OBS connection, Queues, etc).

Also, at the moment, you can only copy 1 sub-action, this may change in the future when I start enabling multi-select capabilities, but, it's 1 step at a time.

## New Sub-Actions

### Subscriber Only
This will let you enable or disable Subscriber Only mode for your channel

### Emote Only
This will let you enable or disable Emote Only mode for your channel

### Read Lines From File
With this sub-action, you'll be able to read all the lines of a file into variables.  It will put each line of the file into `%line#%` where # is the line number starting from 0. `%lineCount%` will also be added with the total number of lines.

### Fetch Url
You can now fetch simple api endpoints and put them into a variable of your choosing. The Url supports variable parsing.

![sub-action-fetch-url-01.png](/sub-action-fetch-url-01.png)

### Pick Color
Added a way to pick a colour and put it on the arguments for an action.

![sub-action-pick-color-01.png](/sub-action-pick-color-01.png)

When this sub-action is run, the follow variables are added to the arguments

| Variables | Description |
|       ---:|-------------|
| `%var.color.a%` | The alpha value |
| `%var.color.r%` | The red value |
| `%var.color.g%` | The gren value |
| `%var.color.b%` | The blue value |
| `%var.html%` | The html color code |
| `%var.htmlalpha%` | The html color code with alpha value |
| `%var.obs%` | The color as an OBS ABGR value |

> This may evolve a bit in the future, either by way of more capabilities, or moving it to a different area
{.is-info}

### Comment
Just an action that you can put text into, that'll show up as a comment, pre and post fixed with **, it will not be executed when the action is run.

## New C# Methods
2 new methods are available for enabling/disabling Subscriber/Emote only modes
```csharp
void TwitchSubscriberOnly(bool enabled = true);
void TwitchEmoteOnly(bool enabled = true);
```

## Groups
The groups section has had a few updates.  The list of groups has been udpated with some context menu options.  You can toggle the Bot status of a group, delete, clear a group; as well as export a group to a file, and import from a file.

There is more work to be done here. These are the first steps.

## Find Refs
Using the Jokes code that is in the examples channel of the discord, I went through and tried to get **Streamer.bot** to be a bit more lenient on how it adds/removes references when you click the Find Refs button on the Execute C# Code dialog.  It is still not perfect, nor will it ever be, as trying to "figure" out what references are required is not an easy thing to do without it taking a while.


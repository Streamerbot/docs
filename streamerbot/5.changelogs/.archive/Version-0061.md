---
title: Version 0.0.61
description: 
published: true
date: 2022-11-11T17:02:34.519Z
tags: 
editor: markdown
dateCreated: 2022-02-14T20:25:07.288Z
---

* Fix running action from C#, possible caught crash and the action would not run
* Fix crash when editing play sound from folder, when folder no longer exists
* Fix editing channel rewards, global cooldown limit was too low causing a crash
* Fix custom server sockets, sending data was not working correctly
* Fix FileWatcher, had a few typos with menu interactions
* Collapsed groups in actions and commands will be remembered and set on launch
* More fixes I probably forgot
{.changelog-fixes}

<span></span>

* Update commands to allow groups to be collapsible.
* Updated Execute C# Method sub-action to run on UI thread
* Update actions list with groups, actions are sorted and groups can be collapsed
* Update cheers not being included in credits
* First pass of updating groups for future changes, this converts and alters underlying data
* More updates I probably forgot
{.changelog-updates}

<span></span>

* Add ability to enable/disable actions, along with a new sub-action to set an actions state and C# methods
* Add new menu item when right clicking on sub-action to provide capabilities to run certain methods tied to the sub-action
* Add a few new menu options to copy the IDs of Actions and Commands
* Add new options to Execute C# Code to support delayed start
{.changelog-new}

# New Features
## Sub-Actions
As an experiment, I am adding new custom menu item to run certain methods contained within a sub-action.  At this moment, this only applies to Execute C# Code, there are 2 new menu items to Compile, and Unload; which will trigger a compile and init of the code, or it will fully unload/dispose of the code (like what happens in a shutdown)

## Execute C# Code
There is a new option for a delayed start, as well as an option to run a method on a UI thread.  The reason for this addition is, you're able to us WinForms and create fully backed UI code.  But to do this, anything WinForm related **MUST** originate from a UI thread.  This usage is fairly advanced, so if you're in a position to do this, then you'll understand more.

I have added 3 methods to be able to create and end Twitch Polls

```csharp
bool TwitchPollCreate(string title, List<string> choices, int duration, int bitsPerVote = 0, int channelPointsPerVote = 0);
void TwitchPollTerminate(string pollId);
void TwitchPollArchive(string pollId);
```

Added 2 new methods that will allow you to enable/disable actions

```csharp
void DisableAction(string actionName);
void EnableAction(string actionName);
```
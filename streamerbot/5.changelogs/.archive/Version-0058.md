---
title: Version 0.0.58
description: 
published: true
date: 2023-06-11T15:00:22.927Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:36:36.285Z
---

* Misc fixes/updates
* Fix how Twitch authorization happens, it now forces an authorize each time instead of only the first time, so you can easily switch accounts
* Fix for 3rd party emotes not being handled correctly for /me actions
* 5xx errors from Twitch API were not being handled properly, causing a crash, they should be handled now
* Fix Set Global sub-action not working when you try to set a specific value
* Fix Set Time State sub-action, not being able to select a timer
* Fix a potential crash when deleting a reward with an action attached, then renaming that action afterwards
{.changelog-fixes}

<span></span>

* FirstWords are now cached, so on a bot restart/crash they won't happen again, this is setup the same way as credits and the reset duration can be configured
* Update permissions for Commands, groups and user permissions can be combined now. Also added a grant type for allow/deny
* Updated Twitch Timeout sub-action, Exclude Moderators now applies to Redeemer option
{.changelog-updates}

<span></span>

* Add new sub-action to put a random number in the arguments
* Add new option to Commands, Ignore Bot Account, which will ignore the command if it's coming from your setup bot account
* Add new Execute C# functions for adding/removing users to/from groups
* Added a missing scope for twitch bot account, this will require a re-authorization
* Add a `Default Value` option to Get Global sub-action
{.changelog-new}

## New Random Number Sub-Action
You can use this sub-action to get a random number between 2 values which will put `%randomNumber%` as a new variable, or the next float value which will put `%randomFloat%` and `%randomPercent%` in the arguments.

## Command Permissions
Added a new Grant Type, this can be Allow, or Deny, which will alter how the permission lists work.

Allow is the default behaviour, and if both permission lists are empty, then anyone can use the command.  If either permission list has a group, or a user in it, then the user must be in the group, or in the explicit user list to be able to use the command.

Deny is a new option, if this is selected, and both permission lists are empty, then everyone is denied from using the command.  If either permission list has a group or a user in it, and the user trying to activate the command exists in the group, or user list, then they will not be allowed to use the command.

## New Execute C# Methods
Added a few functions to deal with adding/removing users from groups

```csharp
bool UserInGroup(int userId, string groupName);
bool UserInGroup(string userName, string groupName);
bool AddUserToGroup(int userId, string groupName);
bool AddUserToGroup(string userName, string groupName);
bool RemoveUserFromGroup(int userId, string groupName);
bool RemoveUserFromGroup(string userName, string groupName);
```

## GetGlobal Default Value
Added in the ability to specify a default value for Get Global sub-action.

When this is not set, it will behave as it has in past versions.

If there is a default value set, and the variable is not found, it will return this value, as well as set the variable to this value
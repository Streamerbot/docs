---
title: Commands
description: Modify chat commands and their cooldowns with C# code
---

## State
### `EnableCommand`
Enable an existing command
::code-group
  ```csharp [Method]
  void EnableCommand(string id);
  ```
  ```csharp [Example]
  // Enable the "shoutout" command
  CPH.EnableCommand("shoutout");
  ```
::

### `DisableCommand`
Disable an existing command
::code-group
  ```csharp [Method]
  void DisableCommand(string id);
  ```
  ```csharp [Example]
  // Disable the "shoutout" command
  CPH.DisableCommand("shoutout");
  ```
::

## Global Cooldowns
### `CommandSetGlobalCooldownDuration`
Set the global cooldown duration for a command, in seconds
::code-group
  ```csharp [Method]
  void CommandSetGlobalCooldownDuration(string id, int seconds);
  ```
  ```csharp [Example]
  // Set the "shoutout" command global cooldown duration to 10 seconds
  CPH.CommandSetGlobalCooldownDuration("shoutout", 10);
  ```
::

### `CommandAddToGlobalCooldown`
Add seconds to the current active global cooldown of a command
::code-group
  ```csharp [Method]
  void CommandAddToGlobalCooldown(string id, int seconds);
  ```
  ```csharp [Example]
  // Add 10 seconds to the current "shoutout" command cooldown
  CPH.CommandAddToGlobalCooldown("shoutout", 10);
  ```
::

### `CommandResetGlobalCooldown`
Reset the global cooldown for a command to its **initial duration**

::list{type=warning}
- This does **not** set the cooldown to zero
::

::code-group
  ```csharp [Method]
  void CommandResetGlobalCooldown(string id);
  ```
  ```csharp [Example]
  // Reset the cooldown for the "shoutout" command
  CPH.CommandResetGlobalCooldown("shoutout");
  ```
::

### `CommandRemoveGlobalCooldown`
Remove any active global cooldown for a command

::list{type=success}
- Effectively, this will make the command immediately usable again
::

::code-group
  ```csharp [Method]
  void CommandRemoveGlobalCooldown(string id);
  ```
  ```csharp [Example]
  // Remove any active cooldown for the "shoutout" command
  CPH.CommandRemoveGlobalCooldown("shoutout");
  ```
::

## User Cooldowns
### `CommandSetUserCooldownDuration`
Set the user cooldown duration for a command, in seconds
::code-group
  ```csharp [Method]
  void CommandSetUserCooldownDuration(string id, int seconds);
  ```
  ```csharp [Example]
  // Set the "shoutout" command user cooldown to 10 seconds
  CPH.CommandSetUserCooldownDuration("shoutout", 10);
  ```
::

### `CommandAddToUserCooldown`
Add seconds to the current active cooldown of a command, for a specific user
::code-group
  ```csharp [Method]
  void CommandAddToUserCooldown(string id, string userId, int seconds);
  ```
  ```csharp [Example]
  // Add 10 seconds to the current "shoutout" command cooldown for user "streamerbot"
  CPH.CommandAddToUserCooldown("shoutout", "streamerbot", 10);
  ```
::

### `CommandAddToAllUserCooldowns`
Add seconds to the current active cooldown of a command, for all users
::code-group
  ```csharp [Method]
  void CommandAddToAllUserCooldowns(string id, string userId, int seconds);
  ```
  ```csharp [Example]
  // Add 10 seconds to the current "shoutout" command cooldown for all users
  CPH.CommandAddToAllUserCooldowns("shoutout", 10);
  ```
::

### `CommandResetUserCooldown`
Reset the user cooldown for a command to its **initial duration**, for a specific user

::list{type=warning}
- This does **not** set the cooldown to zero - use `CommandRemoveGlobalCooldown` to remove cooldowns
::

::code-group
  ```csharp [Method]
  void CommandResetUserCooldown(string id, string userId);
  ```
  ```csharp [Example]
  // Reset the cooldown for the "shoutout" command, for the "streamerbot" user
  CPH.CommandResetUserCooldown("shoutout", "streamerbot");
  ```
::

### `CommandResetAllUserCooldowns`
Reset the user cooldown for a command to its **initial duration**, for all users

::list{type=warning}
- This does **not** set the cooldown to zero
::

::code-group
  ```csharp [Method]
  void CommandResetAllUserCooldowns(string id);
  ```
  ```csharp [Example]
  // Reset the cooldown for the "shoutout" command, for all users
  CPH.CommandResetAllUserCooldowns("shoutout");
  ```
::

### `CommandRemoveUserCooldown`
Remove any active user cooldowns for a command, for a specific user
::code-group
  ```csharp [Method]
  void CommandRemoveUserCooldown(string id, string userId);
  ```
  ```csharp [Example]
  // Remove any active user cooldown for the "shoutout" command, for the "streamerbot" user
  CPH.CommandRemoveUserCooldown("shoutout", "streamerbot");
  ```
::

### `CommandRemoveAllUserCooldowns`
Remove any active user cooldowns for a command
::code-group
  ```csharp [Method]
  void CommandRemoveAllUserCooldowns(string id);
  ```
  ```csharp [Example]
  // Remove any active user cooldowns for the "shoutout" command
  CPH.CommandRemoveAllUserCooldowns("shoutout");
  ```
::
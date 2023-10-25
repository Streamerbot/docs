---
title: Variables
description: C# methods for manipulating arguments and variables
---

## Arguments
::callout{icon=i-mdi-lightbulb color=amber}
Arguments are local variables only available to the currently running action and any subsequent sub-actions
::

### `SetArgument`
Set an argument to be used in subsequent sub-actions
:csharp-method{name=SetArgument}

## Globals
### `GetGlobalVar`
Fetch the current value of a global variable
:csharp-method{name=GetGlobalVar}

### `SetGlobalVar`
Set a global variable value
:csharp-method{name=SetGlobalVar}

### `UnsetGlobalVar`
Unset a global variable value
:csharp-method{name=UnsetGlobalVar}

## User Variables (Twitch)
### `GetTwitchUserVar`
Fetch a variable for a given Twitch user
::code-group
  ```csharp [Method]
  T GetTwitchUserVar<T>(string userName, string varName, bool persisted = true);
  ```
  ```csharp [Example]
  string myTwitchUserVar = CPH.GetTwitchUserVar<string>("streamerbot", "myTwitchUserVar");
  ```
::

### `SetTwitchUserVar`
Set a variable for a given Twitch user
::code-group
  ```csharp [Method]
  void SetTwitchUserVar(string userName, string varName, object value, bool persisted = true);
  ```
  ```csharp [Example]
  CPH.SetTwitchUserVar("streamerbot", "someVariable", "saving this message for later :)");
  ```
::

### `UnsetTwitchUserVar`
Unset a variable for a given Twitch user
::code-group
  ```csharp [Method]
  void UnsetTwitchUserVar(string userName, string varName, bool persisted = true);
  ```
  ```csharp [Example]
  CPH.UnsetTwitchUserVar("streamerbot", "someVariable");
  ```
::

### `UnsetTwitchUser`
Unset all variables for a given Twitch user
::code-group
  ```csharp [Method]
  void UnsetTwitchUser(string userName, bool persisted = true);
  ```
  ```csharp [Example]
  CPH.UnsetTwitchUser("streamerbot");
  ```
::

## User Variables (YouTube)
### `GetYouTubeUserVar`
Fetch a variable for a given YouTube user
::code-group
  ```csharp [Method]
  T GetYouTubeUserVar<T>(string userName, string varName, bool persisted = true);
  ```
  ```csharp [Example]
  string myYouTubeUserVar = CPH.GetYouTubeUserVar<string>("streamerbot", "myYouTubeUserVar");
  ```
::

### `SetYouTubeUserVar`
Set a variable for a given YouTube user
::code-group
  ```csharp [Method]
  void SetYouTubeUserVar(string userName, string varName, object value, bool persisted = true);
  ```
  ```csharp [Example]
  CPH.SetYouTubeUserVar("streamerbot", "someVariable", "saving this message for later :)");
  ```
::

### `UnsetYouTubeUserVar`
Unset a variable for a given YouTube user
::code-group
  ```csharp [Method]
  void UnsetYouTubeUserVar(string userName, string varName, bool persisted = true);
  ```
  ```csharp [Example]
  CPH.UnsetYouTubeUserVar("streamerbot", "someVariable");
  ```
::

### `UnsetYouTubeUser`
Unset all variables for a given YouTube user
::code-group
  ```csharp [Method]
  void UnsetYouTubeUser(string userName, bool persisted = true);
  ```
  ```csharp [Example]
  CPH.UnsetYouTubeUser("streamerbot");
  ```
::


## User Variables (Deprecated)
::callout{color=amber icon=i-mdi-alert}
These methods will be removed in a future version of **Streamer.bot**.<br>
Use the `Twitch` or `YouTube` counterparts, documented above, instead.
::

```csharp
T GetUserVar<T>(string userName, string varName, bool persisted = true);
void SetUserVar(string userName, string varName, object value, bool persisted = true);
void UnsetUserVar(string userName, string varName, bool persisted = true);
void UnsetUser(string userName, bool persisted = true);
```
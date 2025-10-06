---
title: Version 0.0.59
description: 
published: true
date: 2023-06-11T14:58:12.288Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:36:40.187Z
---

* Fix the test button for cheer events, anon toggle will actually work now
* Fix a potential crash when anon events come through that can trigger first words
* Fix `CPH.Wait(int)`, underlying code was incorrect and crashing silently
* Fix `CPH.PauseReward`, `CPH.UnPauseReward` and the sub-action for this, was calling enable not pause
* Fix permissions for Commands, small logic error
{.changelog-fixes}

<span></span>

* Remove broadcaster account from top channel point users in GetCredits
* Update commands, specifically Starts With, it now adds a space when it checks, so it treats it like an argument based, instead of `!test` matching both `!test` and `!test123`
{.changelog-updates}

<span></span>

* Add new HTTP Get method to reset FirstWords cache
* Add new methods to Execute C# to reset Credits and FirstWords
* Add a new anonymous argument for cheer, gift sub and gift bombs
* Add new right click menu item on rewards, to copy the reward id, for use in C# code
* Add ability to create custom websocket servers (supported solely by C#)
{.changelog-new}

## HTTP Server
I've added a new GET method, ClearFirstWordsCache, this will reset your first words cache

## Custom Websocket Server
Create a custom websocket server to have complete control over what gets sent

Arguments available are `%sessionId%`, `%ip%` on all events, and `%data%` for the message event.  `%data%` will always be passed as a string.

## Execute C# Code
I've gone ahead and added 2 new methods to the C# code that will let you reset the credits and the first words cache.

```csharp
void ResetCredits();
void ResetFirstWords();
```

Added 2 more methods to hide filters on source/scenes, to mirror the sub-action that exists for these.

```csharp
void ObsHideSourcesFilters(string scene, string source, int connection = 0);
void ObsHideScenesFilters(string scene, int connection = 0);
```

Also added a handful of new methods to support custom websocket servers.
```csharp
void WebsocketCustomServerStart(int connection = 0);
void WebsocketCustomServerStop(int connection = 0);
bool WebsocketCustomServerIsListening(int connection = 0);
void WebsocketCustomServerCloseAllSessions(int connection = 0);
void WebsocketCustomServerCloseSession(string sessionId, int connection = 0);
void WebsocketCustomServerBroadcast(string data, string sessionId, int connection = 0);
```
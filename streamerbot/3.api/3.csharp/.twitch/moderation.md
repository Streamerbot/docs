---
title: Moderation
description: Moderate your Twitch chat with code actions
---

## Timeout
### `TwitchTimeoutUser`
:csharp-method{name=TwitchTimeoutUser}
::callout{icon=i-mdi-alert color=amber}
A duration of `0` will effectively **result in a ban**
::

## Ban
### `TwitchBanUser`
:csharp-method{name=TwitchBanUser}

### `TwitchUnbanUser`
:csharp-method{name=TwitchUnbanUser}
::callout{color=amber icon=i-mdi-lightbulb}
This method will both **unban and untimeout** the specified user
::

## Chat Mode
### `TwitchSubscriberOnly`
:csharp-method{name=TwitchSubscriberOnly}

### `TwitchEmoteOnly`
:csharp-method{name=TwitchEmoteOnly}

### `TwitchSlowMode`
:csharp-method{name=TwitchSlowMode}

### `TwitchFollowMode`
:csharp-method{name=TwitchFollowMode}

## Chat Messages
### `TwitchClearChatMessages`
:csharp-method{name=TwitchClearChatMessages}

### `TwitchDeleteChatMessage`
:csharp-method{name=TwitchDeleteChatMessage}
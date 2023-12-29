---
title: Shoutout Created
description: Trigger for when a Twitch Shoutout is Created
version: 0.1.14
twitchService: Chat Client
variables:
  - name: shoutoutId
    type: string
    description: Twitch's internal ID for the shoutout
  - name: targetUserId
    type: string
    description: The user's id
    value: a126e8a8-43f7-4a14-8990-e8c3feea76d8
  - name: targetUserLogin
    type: string
    description: The target user's login name
    value: twitchuser123
  - name: targetUserDisplayName
    type: string
    description: The target user's display name
    value: TwitchUser123
  - name: targetUserPrimaryColorHex
    type: string
    description: The target user's primary chat color
    value: #e5e5e5
  - name: targetUserProfileImageURL
    type: string
    description: The user's profile image URL
commonVariables:
  - TwitchUser
---

::wip
TODO: Add shared twitch target vars here
::

::callout{icon=i-mdi-lightbulb color=primary}
User Variables: Who created the shoutout
Target Variables: Who reveived the shoutout
::
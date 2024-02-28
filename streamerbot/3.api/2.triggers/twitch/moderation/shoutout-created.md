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
    value: 718933593
  - name: targetUserLogin
    type: string
    description: The target user's login name
    value: twitchuser123
  - name: targetUserDisplayName
    type: string
    description: The target user's display name
    value: TwitchUser123
  - name: viewerCount
    type: string
    description: The amount of viewers of the broadcaster's livestream
    value: 60
  - name: cooldownEndsAt
    type: DateTime
    description: The timestamp the cooldown to send another shoutout ends at
    value: 8/4/2023 10:56:06 AM
  - name: targetCooldownEndsAt
    type: DateTime
    description: The timestamp the cooldown to send a shoutout to the same user ends at
    value: 8/4/2023 10:56:06 AM
commonVariables:
  - TwitchUser
---

::wip
TODO: Add shared twitch target vars here
::

::tip{color=primary}
User Variables: Who created the shoutout
Target Variables: Who received the shoutout
::
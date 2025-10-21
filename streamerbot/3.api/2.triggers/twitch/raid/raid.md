---
title: Raid
description: Trigger for when you get raided on Twitch
version: 0.0.33
twitchService: Chat Client
parameters:
  - name: Range
    import: common/range
variables:
  - name: viewers
    type: number
    description: The amount of viewers this raid received
    value: 183
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
---

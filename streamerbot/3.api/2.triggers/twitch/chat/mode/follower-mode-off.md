---
title: Follower Mode Off
description: Trigger for when the Twitch Follower Mode is turned Off
version: 0.2.3
twitchService: Chat Client
variables:
  - name: followerMode
    type: boolean
    description: The follower mode
    value: False
  - name: followerModeDuration
    type: number
    description: The follower mode duration
    value: 0
commonVariables:
  - TwitchBroadcaster
---

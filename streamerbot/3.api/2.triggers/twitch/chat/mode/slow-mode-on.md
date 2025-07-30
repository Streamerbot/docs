---
title: Slow Mode On
description: Trigger for when the Twitch Slow Mode is turned On
version: 0.2.3
twitchService: Chat Client
variables:
  - name: slowMode
    type: boolean
    description: The slow mode
    value: True
  - name: slowModeWaitTime
    type: number
    description: The slow mode duration
    value: 23
commonVariables:
  - TwitchBroadcaster
---

---
title: Sub Counter Rollover
description: Trigger for a Twitch Sub Counter Rollover
twitchService: Chat Client
variables:
  - name: subCounter
    type: number
    description: The current value of the sub counter
    value: 20
  - name: rollover
    type: number
    description: The configured rollover value
    value: 50
  - name: rolloverCount
    type: number
    description: The number of times the configured rollover value has been reached
    value: 3
---
---
title: Community Goal Ended
description: Trigger for when a Twitch Community Goal Ends
twitchService: PubSub
removed: 1.0.0
variables:
  - name: title
    type: string
    description: The name of the community goal
    value: My community goal
  - name: goalAmount
    type: number
    description: The total amount required to complete the goal
  - name: goalAmountFormatted
    type: number
    description: The total amount required to complete the goal as a formatted number
  - name: contributed
    type: number
    description: The amount that has been contributed to the goal so far
  - name: contributedFormatted
    type: number
    description: The amount that has been contributed to the goal so far as a formatted number
  - name: percentComplete
    type: string
    description: The percentage that the goal has completed
    value: 73%
  - name: percentDecimal
    type: number
    description: The percentage that the goal has completed as a decimal
    value: 0.73
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
---

::caution
**Removed in Streamer.bot v1.0.0**
<br>
Twitch has deprecated the PubSub API and all triggers relying on it have been removed.
::
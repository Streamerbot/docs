---
title: Shared Resub
description: Triggered When a User Resubscribes in the Shared Chat
twitchService: EventSub
version: 0.2.5
variables:
  - name: tier
    type: string
    description: The subscription tier<br>`prime`, `tier 1`, `tier 2`, `tier 3`
    value: tier 1
  - name: monthStreak
    type: number
    description: The current subscription streak of the user
    value: 5
  - name: cumulative
    type: number
    description: The amount of cumulative months that the user is subscribed for
    value: 2
  - name: streakShared
    type: boolean
    version: 0.2.5
    description:  Returns whether or not the user shares their resub streak.
    value: true
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
  - TwitchChat
  - TwitchSharedChatSource
---

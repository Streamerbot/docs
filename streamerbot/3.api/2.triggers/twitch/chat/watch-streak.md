---
title: Watch Streak
description: Triggers when a user shares their watch streak
twitchService: Chat Client
version: 0.2.4
parameters:
  - name: Range
    type: Select
    required: true
    description: |
      :range-description
variables:
  - name: systemMessage
    type: string
    description: Twitch's internal watch streak message
    value: Tommi3006 watched 5 consecutive streams this month and sparked a watch streak!
  - name: watchStreak
    type: int
    description: the watch streak count
    value: 5
  - name: copoReward
    type: int
    description: The rewarded channel points for the watch streak
    value: 450
  - name: watchStreakId
    type: string
    description: ID of the watch streak
    value: c947cc8a-f458-499b-af5e-d439cc857235
commonVariables:
  - TwitchUser
  - TwitchChat    
---



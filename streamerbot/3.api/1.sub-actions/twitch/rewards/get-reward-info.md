---
title: Get Reward Info
description: Get the info from a reward.
parameters:
  - name: Reward
    type: Select
    required: true
    description: Choose the reward where you want to get the info from.
variables:
  - name: rewardId
    type: string
    description: The unique identifier for the reward
    value: 44e86f71-8ace-4739-a123-3ff095489343
  - name: rewardCost
    type: number
    description: The cost of the reward
    value: 200
  - name: rewardTitle
    type: string
    description: The name of the reward
    value: My Reward
  - name: rewardBackgroundColor
    type: string
    description: The background color of the reward, in hex format
    value: "#FFFF00"
  - name: rewardEnabled
    type: bool
    description: If the reward is enabled
    value: True
  - name: rewardPaused
    type: bool
    description: If the reward is paused
    value: False
  - name: rewardPrompt
    type: string
    description: The description of the reward
    value: My Reward description
  - name: rewardSkipRequestQueue
    type: bool
    description: Whether or not the Reward is auto completed when redeemed
    value: False
  - name: rewardMaxPerStream
    type: number
    description: How many total redemptions can be done per stream, 0 means no limit
    value: 0
  - name: rewardMaxPerUserPerStream
    type: number
    description: How many redemptions each user can make per stream, 0 means no limit
    value: 0
  - name: rewardGlobalCooldown
    type: number
    description: The global cooldown of the Reward in seconds
    value: 0
  - name: rewardIsOurs
    type: bool
    description: If the reward is owned by Streamer.bot and can be updated by sub-actions
csharpMethods:
  - TwitchGetRewards
---

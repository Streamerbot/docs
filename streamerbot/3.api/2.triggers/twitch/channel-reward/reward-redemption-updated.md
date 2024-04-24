---
title: Reward Redemption Updated
description: Trigger for a Twitch Reward Redemption when it's marked as complete or rejected in Twitch Reward Queue.
version: 0.2.0
twitchService: PubSub
variables:
  - name: redemptionId
    type: string
    description: The unique identifier for the reward redemption
    value: 4d9f236b-7486-481a-89af-1d03676d5275
  - name: rewardId
    type: string
    description: The unique identifier for the reward
    value: 44e86f71-8ace-4739-a123-3ff095489343
  - name: rewardName
    type: string
    description: The name of the reward
    value: My Reward
  - name: rewardPrompt
    type: string
    description: The description of the reward
    value: My Reward description
  - name: rewardCost
    type: number
    description: The cost of the reward
    value: 200
  - name: rewardStatus
    type: string
    description: Whether the reward was marked as complete/rejected.
    value: `fulfilled` or `canceled`
  - name: rawInputEscaped
    type: string
    description: The text entered by the user (if enabled)
    value: https://streamer\.bot/Test Escaped Text \$\$\$
commonVariables:
  - TwitchUser
parameters:
  - name: Reward
    type: Select
    required: true
    default: Any
    description: |
      Select a configured Twitch reward
      - Select `Any` to trigger on **any reward**
  
      ::tip
      You can quickly register a new reward by clicking the `Create Reward` button!
      ::
---

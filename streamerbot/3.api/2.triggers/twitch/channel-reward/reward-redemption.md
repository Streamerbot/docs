---
title: Reward Redemption
description: Trigger for a Twitch Reward Redemption
version: 0.0.30
twitchService: EventSub
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
  - name: counter
    type: number
    description: The amount of times the reward has been used
    value: 53
  - name: userCounter
    type: number
    description: The amount of times the reward has been used by this user
    value: 8
  - name: rawInput
    type: string
    description: The text entered by the user (if enabled)
    value: https://streamer.bot/Test Unescaped Text $$$
  - name: rawInputEscaped
    type: string
    description: The text entered by the user (if enabled)
    value: https://streamer\.bot/Test Escaped Text \$\$\$
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
---

## Parameters
::field-group
  ::field{name=Reward type=Select required}
    Select a configured Twitch reward
    - Select `Any` to trigger on **any reward**

    ::tip{color=amber}
    You can quickly register a new reward by clicking the `Create Reward` button!
    ::
  ::
::
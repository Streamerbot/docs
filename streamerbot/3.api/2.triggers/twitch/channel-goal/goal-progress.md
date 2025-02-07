---
title: Goal Progress
description: Trigger for the progression of a Twitch goal
version: 0.1.15
twitchService: EventSub
variables:
  - name: goal.id
    type: string
    description: The unique id of this channel goal
  - name: goal.type
    type: string
    description: The type of this channel goal
    value: |
      `follow`/`subscription`/`new_subscription`/`new_subscription_count`/`new_bit`/`new_cheerer`
  - name: goal.description
    type: string
    description: The description of this channel goal
  - name: goal.currentAmount
    type: number
    description: The current amount of this channel goal
  - name: goal.targetAmount
    type: number
    description: The target of this channel goal
  - name: goal.startedAt
    type: DateTime
    description: The timestamp that the channel goal started
    value: 8/4/2023 10:56:06 AM
---
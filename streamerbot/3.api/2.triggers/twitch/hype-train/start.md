---
title: Hype Train Starts
description: Trigger for when a Twitch Hype Train Starts
twitchService: EventSub
variables:
  - name: level
    type: number
    description: The current Hype Train level
    value: 3
  - name: startedAt
    type: DateTime
    description: The time the hype train started
    value: 8/4/2023 10:56:06 AM
  - name: expiresAt
    type: DateTime
    description: The time that the hype train expires
    value: 8/4/2023 10:56:06 AM
  - name: duration
    type: DateTime
    description: The duration of the hype train
    value: 120
  - name: percent
    type: number
    description: The percentage of the current level
    value: 80%
  - name: percentDecimal
    type: number
    description: The percentage of the current level as a decimal
    value: 0.8
  - name: top.bits.user
    type: string
    description: The top cheerer of this hype train display name
    value: TwitchUser123
  - name: top.bits.userName
    type: string
    description: The top cheerer of this hype train login name
    value: twitchuser123
  - name: top.bits.userId
    type: number
    description: The top cheerer of this hype train user id
    value: a126e8a8-43f7-4a14-8990-e8c3feea76d8
  - name: top.bits.total
    type: number
    description: The amount of bits donated from the the top cheerer this hype train
    value: 1500
  - name: top.subscription.user
    type: string
    description: The top sub gifter of this hype train display name
    value: TwitchUser123
  - name: top.subscription.userName
    type: string
    description: The top sub gifter of this hype train login name
    value: twitchuser123
  - name: top.subscription.userId
    type: number
    description: The top sub gifter of this hype train user id
    value: a126e8a8-43f7-4a14-8990-e8c3feea76d8
  - name: top.subscription.total
    type: number
    description: The amount of giftsubs donated from the the top gift subber this hype train
    value: 10
  - name: top.other.user
    type: string
    description: The user display name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
    value: TwitchUser123
  - name: top.other.userName
    type: string
    description: The user login name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
    value: twitchuser123
  - name: top.other.userId
    type: number
    description: The user id of the user that have given the most amount of things that aren't bits/giftsubs this hype train
    value: a126e8a8-43f7-4a14-8990-e8c3feea76d8
  - name: top.other.total
    type: number
    description: The toal amount of the user that have given the most amount of things that aren't bits/giftsubs this hype train
    value: 10
  - name: id
    type: string
    description:  The unique identifier of the hype train
---
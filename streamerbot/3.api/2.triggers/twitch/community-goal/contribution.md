---
navigation.title: Contribution
title: Community Goal Contribution
description: Trigger for a Twitch Community Goal Contribution
twitchService: PubSub
variables:
  - name: title
    type: string
    description: The name of the community goal
    value: My community goal
  - name: userContributed
    type: number
    description: The amount that the user has contributed
  - name: userContribFormatted
    type: number
    description: The amount that the user has contributed as a formatted number
  - name: userTotalContributed
    type: number
    description: The total amount that the user has contributed
  - name: userTotalContribFormatted
    type: number
    description: The formatted total amount the user has contributed
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
  - name: durationDays
    type: number
    description: The total duration of this community goal in days
    value: 7
  - name: daysLeft
    type: number
    description: The amount of days left for this community goal
    value: 3
commonVariables:
  - TwitchUser
---
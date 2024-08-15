---
title: Resubscription
description: Trigger for a Twitch Resubscription
twitchService: Chat Client
parameters:
  - name: Tier
    type: Checkbox
    description: |
      Choose on which tier to trigger the gift bomb

      Options: `Tier 1`, `Tier 2`, `Tier 3`
  - name: Range
    type: Select
    description: |
      :range-description
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
  - name: isMultiMonth
    type: bool
    description: If subscription is for longer then one month
    value: True
  - name: multiMonthDuration
    type: int
    description: The amount of months subscribed for
    value: 2
  - name: multiMonthTenure
    type: int
    description: The total amount of months subscribed for
    value: 3
commonVariables:
  - TwitchUser
  - TwitchChat
---

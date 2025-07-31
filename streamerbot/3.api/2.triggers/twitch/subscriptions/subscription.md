---
title: Subscription
description: Trigger for a Twitch Subscription
twitchService: EventSub
parameters:
  - name: Tier
    type: Checkbox
    description: |
      Choose on which tier to trigger the gift bomb

      Options: `Prime`, `Tier 1`, `Tier 2`, `Tier 3`
variables:
  - name: tier
    type: string
    description: The subscription tier<br>`prime`, `tier 1`, `tier 2`, `tier 3`
    value: tier 1
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
    description: How many months of the multi-month subscription have passed so far
    value: 1
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
  - TwitchChat
---

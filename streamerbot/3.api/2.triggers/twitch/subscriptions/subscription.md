---
title: Subscription
description: Trigger for a Twitch Subscription
twitchService: Chat Client
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
    description: The total amount of months subscribed for
    value: 3
commonVariables:
  - TwitchUser
  - TwitchChat
---

## Parameters
::field-group
  ::field{name=Tier type=Checkbox}
    Choose on which tier to trigger the subscription
    - Options:
      - Prime
      - Tier 1
      - Tier 2
      - Tier 3
  ::
::

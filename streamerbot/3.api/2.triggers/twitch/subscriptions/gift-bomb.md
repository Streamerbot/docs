---
title: Gift Bomb
description: Trigger for a Twitch Gift Bomb
twitchService: Chat Client
variables:
  - name: gifts
    type: number
    description: The number of subscriptions in this gift bomb
    value: 10
  - name: totalGifts
    type: number
    description: The total number of subscriptions gifted by the user.
    value: 42
  - name: fromGiftBomb
    type: boolean
    description: Are the subscriptions from a gift bomb?
    value: True
  - name: anonymous
    type: boolean
    description: Is the gift bomb anonymous?
    value: False
  - name: tier
    type: string
    description: The subscriptions tier<br>`tier 1`, `tier 2`, `tier 3
    value: tier 1
commonVariables:
  - TwitchUser
---

## Parameters
::field-group
  ::field{name=Tier type=Checkbox}
    Choose on which tier to trigger the gift bomb
    - Options:
      - Tier 1
      - Tier 2
      - Tier 3
  ::
  ::field{name="Sub Type" type=Checkbox}
    Choose on which sub types to trigger the gift bomb
    - Options:
      - Public
      - Anonymous
  ::
  ::field{name=Range type=Range}
    :range-description
  ::
::
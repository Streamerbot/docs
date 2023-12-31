---
title: Gift Subscription
description: Trigger for a Twitch Gift Subscription
twitchService: Chat Client
variables:
  - name: recipientUser
    type: string
    description: The recipient user's display name
    value: TwitchUser123
  - name: recipientUserName
    type: string
    description: The recipient user's login name
    value: twitchuser123
  - name: recipientId
    type: string
    description: The recipient user's id
  - name: totalSubsGifted
    type: number
    description: The total amount of subscriptions that the user has gifted
    value: 24
  - name: monthsGifted
    type: number
    description: The number of prepaid months that the user has gifted<br>`1`, `3`, `6`, `12`
    value: 6
  - name: fromGiftBomb
    type: boolean
    description: Is this from a gift bomb?
    value: True
  - name: subBombCount
    type: number
    description: The amount of gift subs in the gift bomb
    value: 10
  - name: cumulativeMonths
    type: number
    description: The amount of months the recipient has been subscribed to the channel
    value: 1
  - name: anonymous
    type: boolean
    description: Is the gift sub anonymous?
    value: False
  - name: tier
    type: string
    description: The subscription tier<br>`tier 1`, `tier 2`, `tier 3
    value: tier 1
commonVariables:
  - TwitchUser
---

## Parameters
::field-group
  ::field{name=Tier type=Checkbox required}
    Choose on which tier to trigger the gift sub
    - Options:
      - Tier 1
      - Tier 2
      - Tier 3
  ::
  ::field{name="Sub Type" type=Checkbox required}
    Choose on which sub types to trigger the gift sub
    - Options:
      - Public
      - Anonymous
  ::
  ::field{name="Months Gifted" type=Checkbox required}
    Choose on how much months gifted to trigger the gift sub
    - Options:
      - 1
      - 3
      - 6
      - 12
  ::
  ::field{name=Range type=Range}
    :range-description
  ::
::
---
title: Gift Bomb
description: Trigger for a Twitch Gift Bomb
twitchService: EventSub
parameters:
  - name: Tier
    type: Checkbox
    description: |
      Choose on which tier to trigger the gift bomb

      Options: `Tier 1`, `Tier 2`, `Tier 3`
  - name: Sub Type
    type: Checkbox
    description: |
      Choose on which sub types to trigger the gift bomb

      Options: `Public`, `Anonymous`
  - name: Range
    type: Select
    description: |
      :range-description
variables:
  - name: gifts
    type: number
    description: The number of subscriptions in this gift bomb
    value: 10
  - name: totalGifts
    type: number
    description: The total number of subscriptions gifted by the user.
    value: 42
  - name: gift.cumulativeMonths.#
    type: number
    description: Cumulative months the user has been subscribed for.<br># is a number starting at 0 til totalGifts - 1
    value: 1
  - name: gift.recipientUser.#
    type: string
    description: Display name of the gifted user<br># is a number starting at 0 til totalGifts - 1
    value: User0
  - name: gift.recipientUserName#
    type: string
    description: Login name of the gifted user<br># is a number starting at 0 til totalGifts - 1
    value: user0
  - name: gift.recipientId#
    type: string
    description: Id of the gifted user<br># is a number starting at 0 til totalGifts - 1
    value: 123456789
  - name: anonymous
    type: boolean
    description: Is the gift bomb anonymous?
    value: False
  - name: tier
    type: string
    description: The subscriptions tier<br>`tier 1`, `tier 2`, `tier 3`
    value: tier 1
  - name: systemMessage
    type: string
    version: 0.2.5
    description: The system message that was put into Twitch Chat.
    value: Here's another gifted sub for your channel!
  - name: totalSubsGiftedShared
    type: boolean
    version: 0.2.5
    description:  A boolean value if the user gifting the sub(s) shares there total gift count.
    value: true
commonVariables:
  - TwitchUser
---

---
title: Shared Sub Gift
description: Triggered When a User Gifts a Subscription in a Shared Chat
twitchService: EventSub
version: 0.2.5
variables:
  - name: tier
    type: string
    description: The subscription tier<br>`prime`, `tier 1`, `tier 2`, `tier 3`
    value: tier 1
  - name: anonymous
    type: boolean
    description: Returns whether or not the sub was gifted anonymously
    value: False
  - name: totalSubsGifted
    type: number
    description: The total amount of subscriptions that the user has gifted
    value: 24
  - name: monthsGifted
    type: number
    description: The number of prepaid months that the user has gifted<br>`1`, `3`, `6`, `12`
    value: 6
  - name: cumulativeMonths
    type: number
    description: The amount of months the recipient has been subscribed to the channel
    value: 2
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
    description: The recipient user's ID
  - name: fromGiftBomb
    type: boolean
    description: Is this from a gift bomb?
    value: False
  - name: subBombCount
    type: number
    description: The amount of gift subs in the gift bomb
    value: 0
commonVariables:
  - TwitchUser
  - TwitchChat
  - TwitchSharedChatSource
---

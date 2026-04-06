---
title: Mass Gift Subscription
description: Trigger for a Kick Mass Gift Subscription
variables:
  - name: recipient.#.userName
    type: string
    description: The recipient user's display name<br># is a number starting at 0
    value: KickUser123
  - name: recipient.#.userLogin
    type: string
    description: The recipient user's login name<br># is a number starting at 0
    value: kickuser123
  - name: recipient.#.userId
    type: string
    description: The recipient user's id<br># is a number starting at 0
  - name: recipient.#.profilePicture
    type: string
    description: The recipient user's profile picture<br># is a number starting at 0
  - name: recipient.#.platform
    type: string
    description: The recipient user's platform<br># is a number starting at 0
  - name: subscribedAt
    type: DateTime
    description: Subcription timestamp
  - name: expiresAt
    type: DateTime
    description: Subcription expiration timestamp (subscribedAt + 1 month)
commonVariables:
  - KickBroadcaster
  - KickUser
---

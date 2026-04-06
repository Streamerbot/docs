---
title: Gift Subscription
description: Trigger for a Kick Gift Subscription
variables:  
  - name: recipient.userName
    type: string
    description: The recipient user's display name
    value: KickUser123
  - name: recipient.userLogin
    type: string
    description: The recipient user's login name
    value: kickuser123
  - name: recipient.userId
    type: string
    description: The recipient user's id
  - name: recipient.profilePicture
    type: string
    description: The recipient user's profile picture
  - name: recipient.platform
    type: string
    description: The recipient user's platform
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

:wip

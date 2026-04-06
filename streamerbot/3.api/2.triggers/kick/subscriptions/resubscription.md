---
title: Gift Resubscription
description: Trigger for a Kick Resubscription
variables:
  - name: expiresAt
    type: DateTime
    description: Subcription expiration timestamp (subscribedAt + 1 month)
  - name: duration
    type: number
    description: The duration of subscription
    value: 1
  - name: badgeCount
    type: number
    description: Number of badges the user has
    value: 1
  - name: monthsSubscribed
    type: number
    description: The amount of months subscribed for
    value: 2
commonVariables:
  - KickBroadcaster
  - KickUser
---

:wip

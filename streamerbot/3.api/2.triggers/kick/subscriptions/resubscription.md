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
  - name: monthsSubscribed
    type: number
    description: The amount of months subscribed for
    value: 2
  - name: badgeCount
    type: number
    description: Number of badges the user has
    value: 1
  - name: badge
    type: List
    description: A C# accessible list of badges used in the chat message
    children:
      - name: badge.#.id
        type: string
        description: Plain text name of the badge
        value: broadcaster
      - name: badge.#.name
        type: string
        description: Unique identifier for the badge
        value: Broadcaster
      - name: badge.#.info
        type: string
        description: URL of the badge image
        value: https://files.kick.com/badges/broadcaster
commonVariables:
  - KickBroadcaster
  - KickUser
---

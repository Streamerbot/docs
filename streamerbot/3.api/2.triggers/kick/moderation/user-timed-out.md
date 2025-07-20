---
title: User Timed Out
description: Trigger for when a Kick User is Timed Out
variables:
  - name: createdAt
    type: DateTime
    description: The timestamp when the timeout was created
    value: 7/19/2025 10:38:24 PM
  - name: createdById
    type: string
    description: The Kick user id from who created the timeout
    value: 11088894
  - name: createdByUsername
    type: string
    description: The Kick user name from who created the timeout
    value: kickmod123
  - name: createdByDisplayName
    type: string
    description: The Kick display name from who created the timeout
    value: KickMod123
  - name: duration
    type: number
    description: The duration of the timeout
    value: 300
  - name: reason
    type: string
    description: The reason for the timeout
    value: My timeout reason
commonVariables:
  - KickUser
  - KickBroadcaster
---
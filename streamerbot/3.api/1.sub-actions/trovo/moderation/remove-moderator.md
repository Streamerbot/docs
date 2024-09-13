---
title: Remove Moderator
description: Creates a clip of the past 90s of your stream
parameters:
  - name: User Login
    type: string
    required: true
    description: The user name of the moderator that you want to remove.  Also supports %variables%
variables:
  - name: unmodResult
    type: boolean
    description: If removing moderator status form the user was successful or not
    value: True
  - name: unmoddedUser
    type: string
    description: The display name of the user that had their moderator status removed
  - name: unmoddedUserName
    type: string
    description: The login of the user that had their moderator status removed
  - name: unmoddedUserId
    type: string
    description: The ID of the user that had their moderator status removed
  - name: unmoddedUserType
    type: string
    description: Platform of the user that had their moderator status removed
    value: trovo
---

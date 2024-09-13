---
title: Add Moderator
description: Adds the specified user as a moderator of your Trovo channel
parameters:
  - name: User Login
    type: string
    required: true
    description: The user's name you want to add as a moderator. Also supports %variables%
variables:
  - name: modResult
    type: boolean
    description: If adding the user as a moderator was successful or not
    value: True
  - name: moddedUser
    type: string
    description: The display name of the user that was added as a moderator
  - name: moddedUserName
    type: string
    description: The login of the user that was added as a moderator
  - name: moddedUserId
    type: string
    description: The ID of the user that was added as a moderator
  - name: moddedUserType
    type: string
    description: Platform of the modded user
    value: trovo
---

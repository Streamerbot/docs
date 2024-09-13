---
title: Unban User
description: Unban a user from your Trovo channel
parameters:
  - name: User Login
    type: string
    required: true
    description: The user name to unban.  Also supports %variables%
variables:
  - name: unbanResult
    type: boolean
    description: If removing the ban on the user was successful or not
    value: True
  - name: unbannedUser
    type: string
    description: The display name of the user that had their ban removed
  - name: unbannedUserName
    type: string
    description: The login of the user that had their ban removed
  - name: unbannedUserId
    type: string
    description: The ID of the user that had their ban removed
  - name: unbannedUserType
    type: string
    description: Platform of the user that had their ban removed
    value: trovo
---

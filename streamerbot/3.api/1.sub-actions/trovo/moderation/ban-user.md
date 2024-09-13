---
title: Ban User
description: Ban the specified user on your Trovo channel
parameters:
  - name: User Login
    type: string
    required: true
    description: The user name that is to be banned.  Also supports %variables%
variables:
  - name: banResult
    type: boolean
    description: If banning the user was successful or not
    value: True
  - name: bannedUser
    type: string
    description: The display name of the user that was banned
  - name: bannedUserName
    type: string
    description: The login of the user that was banned
  - name: bannedUserId
    type: string
    description: The ID of the user that was banned
  - name: bannedUserType
    type: string
    description: Platform of the banned user
    value: trovo
---

---
title: Timeout User
description: Give a user a timeout on your Trovo channel
parameters:
  - name: User Login
    type: string
    required: true
    description: The user name that is to be timed out.  Also supports %variables%
  - name: Duration
    type: string
    required: true
    description: How long the user will be timed out for
variables:
  - name: timeoutResult
    type: boolean
    description: If banning the user was successful or not
    value: True
  - name: timedOutUser
    type: string
    description: The display name of the user that was timed out
  - name: timedOutUserName
    type: string
    description: The login of the user that was timed out
  - name: timedOutUserId
    type: string
    description: The ID of the user that was timed out
  - name: timedOutUserType
    type: string
    description: Platform of the timed out user
    value: trovo
---

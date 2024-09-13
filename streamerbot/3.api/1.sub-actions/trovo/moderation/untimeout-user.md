---
title: UnTimeout User
description: Remove the timeout on a user
parameters:
  - name: User Login
    type: string
    required: true
    description: The user name to remove the timeout on.  Also supports %variables%
variables:
  - name: unTimedOutResult
    type: boolean
    description: If removing the timeout on the user was successful or not
    value: True
  - name: unTimedOutUser
    type: string
    description: The display name of the user that had their timeout removed
  - name: unTimedOutUserName
    type: string
    description: The login of the user that had their timeout removed
  - name: unTimedOutUserId
    type: string
    description: The ID of the user that had their timeout removed
  - name: unTimedOutUserType
    type: string
    description: Platform of the user that had their timeout removed
    value: trovo
---

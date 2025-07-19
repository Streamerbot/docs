---
title: Kick UnTimeout
description: Untimeout a Kick user

parameters:
  - name: User Login
    type: String
    required: true
    description: can be a user name or a variable like `%userName%`
variables:
  - name: unTimedOutUser
    type: string
    description: display name of the untimed-out user
    value: Amouranth
  - name: unTimedOutUserName
    type: string
    description: login name of the untimed-out user
    value: Amouranth
  - name: unTimedOutUserId
    type: string
    description: ID of the untimed-out user
    value: 12345678
  - name: unTimedOutUserType
    type: string
    description: platform of the untimed-out user
    value: kick
  - name: unTimedOutResult
    type: bool
    description: indicator whether the untimeout has been successful or not
    value: True/False
csharpMethods: []
---

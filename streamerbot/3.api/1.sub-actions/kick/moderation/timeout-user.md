---
title: Timeout User
description: Timeout a Kick user
parameters:
  - name: User Login
    type: String
    required: true
    description: Can be a user name or a variable like `%userName%`
  - name: Duration
    type: Int
    required: true
    description: Timeout duration in seconds. `0` is a permanent ban.
variables:
  - name: timedOutUser
    type: string
    description: display name of the timed out user
    value: Amouranth
  - name: timedOutUserName
    type: string
    description: login name of the timed out user
    value: Amouranth
  - name: timedOutUserId
    type: string
    description: ID of the timed out user
    value: 12345678
  - name: timedOutUserType
    type: string
    description: platform of the timed out user
    value: kick
  - name: timeoutResult
    type: bool
    description: indicator whether the timeout has been successful or not
    value: True/False
csharpMethods:
  - KickTimeoutUser
---


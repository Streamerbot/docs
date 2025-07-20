---
title: Warn User
description: Warn a Twitch user
version: 0.2.4
parameters:
  - name: User Login
    type: String
    required: true
    description: can be a user name or a variable like `%userName%`
  - name: Reason
    type: String
    required: false
    description: warn reason
variables:
  - name: warnedUser
    type: string
    description: display name of the warned user
    value: GenericUser
  - name: warnedUserName
    type: string
    description: login name of the warned user
    value: genericuser
  - name: warnedUserId
    type: string
    description: ID of the warned user
    value: 12345678
  - name: warnedUserType
    type: string
    description: platform of the warned user
    value: twitch
  - name: warnedResult
    type: bool
    description: indicator whether the warning has been successful or not
    value: True/False
csharpMethods:
  - TwitchWarnUser
---

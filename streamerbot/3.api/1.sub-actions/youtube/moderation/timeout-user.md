---
title: Timeout User
description: Timeout a YouTube user
version: 0.2.4
parameters:
  - name: Broadcast
    type: select
    description: |
      What broacast to apply the ban to.

      * `All` will aply to all broadcasts
      * `Latest` will apply to the latest broadcast monitored
      * `Variable` uses the fixed `broadcast.id` variable to select the broadcast
    required: true
    value: All
  - name: User Login
    type: string
    required: true
    description: Can be a user name or a variable like `%userName%`
  - name: duration
    type: int
    required: true
    description: The legnth, in seconds of the timeout
variables:
  - name: bannedUser
    type: string
    description: Display name of the timedout user
  - name: bannedUserName
    type: string
    description: Login name of the timedout user
  - name: bannedUserId
    type: string
    description: ID of the timedout user
  - name: bannedUserType
    type: string
    description: Platform of the timedout user
    value: youtube
  - name: timeoutResult
    type: boolean
    description: Indicator whether the timeout was successful or not
    value: True/False
csharpMethods:
  - YouTubeTimeoutUserById
  - YouTubeTimeoutUserByName
---

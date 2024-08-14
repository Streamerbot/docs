---
title: Ban User
description: Ban a YouTube user
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
variables:
  - name: bannedUser
    type: string
    description: Display name of the banned user
  - name: bannedUserName
    type: string
    description: Login name of the banned user
  - name: bannedUserId
    type: string
    description: User ID of the banned user
  - name: bannedUserType
    type: string
    description: Platform of the banned user
    value: twitch
  - name: banResult
    type: boolean
    description: Indicator whether the ban was successful or not
    value: True/False
csharpMethods:
  - YouTubeBanUserById
  - YouTubeBanUserByName
---

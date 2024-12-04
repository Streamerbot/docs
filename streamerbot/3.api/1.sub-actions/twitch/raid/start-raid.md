---
title: Timeout User
description: Timeout a user
version: 0.2.4
parameters:
  - name: User Login
    type: String
    required: true
    description: Can be a user name or a argument like `%userName%`
variables:
  - name: startRaidSuccess
    type: boolean
    description: Whether starting the raid was successful
    value: True / False
csharpMethods:
  - TwitchStartRaidByName
  - TwitchStartRaidByNameById
---
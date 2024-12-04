---
title: Start Raid
description: Start a raid
parameters:
  - name: User Login
    type: String
    required: true
    description: Can be a user name or an argument like `%userName%`
variables:
  - name: startRaidSuccess
    type: boolean
    description: Whether starting the raid was successful
    value: True / False
csharpMethods:
  - TwitchStartRaidByName
  - TwitchStartRaidByNameById
---
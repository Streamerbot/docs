---
title: Unban User
description: Unban a Twitch user
parameters:
  - name: User Login
    type: String
    required: true
    description: can be a user name or a variable like `%userName%`
variables:
  - name: unbannedUser
    type: string
    description: display name of the unbanned user
    value: PewDiePie
  - name: unbannedUserName
    type: string
    description: login name of the unbanned user
    value: pewdiepie
  - name: unbannedUserId
    type: string
    description: ID of the unbanned user
    value: 12345678
  - name: unbannedUserType
    type: string
    description: platform of the unbanned user
    value: twitch
  - name: unbanResult
    type: bool
    description: indicator whether the unban has been successful or not
    value: True/False
---

## C# Usage
:csharp-method{name=TwitchUnbanUser}

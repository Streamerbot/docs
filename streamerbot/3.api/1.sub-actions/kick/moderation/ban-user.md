---
title: Ban User
description: Ban a Kick user
parameters:
  - name: User Login
    type: String
    required: true
    description: can be a user name or a variable like `%userName%`
  - name: Reason
    type: String
    required: false
    description: ban reason
variables:
  - name: bannedUser
    type: string
    description: display name of the banned user
    value: Amouranth
  - name: bannedUserName
    type: string
    description: login name of the banned user
    value: Amouranth
  - name: bannedUserId
    type: string
    description: ID of the banned user
    value: 12345678
  - name: bannedUserType
    type: string
    description: platform of the banned user
    value: kick
  - name: banResult
    type: bool
    description: indicator whether the ban has been successful or not
    value: True/False
csharpMethods:
  - KickBanUser
---
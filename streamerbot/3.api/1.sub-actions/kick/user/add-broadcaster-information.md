---
title: Add Kick Broadcaster Information
description: Fetch user data for the connected Kick broadcaster account
variables:
  - name: broadcastUser
    description: Display name of the broadcaster account
    type: string
    value: Mustached_Maniac
  - name: broadcastUserName
    description: Username of the broadcaster account
    type: string
    value: mustached_maniac
  - name: broadcastUserId
    description: Unique user ID of the broadcaster account
    type: string
    value: 11088894
  - name: broadcastUserType
    description: Platform type of the broadcaster account
    type: string
    value: Kick
  - name: broadcasterProfileUrl
    description: Link to the 300x300px PNG version of the broadcaster's Kick profile image
    type: string
    value: https://files.kick.com/images/user/11088894/profile_image/conversion/4495b495-4753-455c-9434-7debf0b82ba3-fullsize.webp
csharpMethods:
  - KickGetBroadcaster
---

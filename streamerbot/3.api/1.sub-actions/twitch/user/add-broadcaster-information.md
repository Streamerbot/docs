---
title: Add Broadcaster Information
description: Fetch user data for the connected Twitch broadcaster account
variables:
  - name: broadcastUser
    description: Display name of the broadcaster account
    type: string
  - name: broadcastUserName
    description: Username of the broadcaster account
    type: string
  - name: broadcastUserId
    description: Unique user ID of the broadcaster account
    type: string
  - name: broadcastUserType
    description: Twitch
    type: string
  - name: broadcastIsAffiliate
    description: Boolean value indicating if the broadcaster account is a Twitch affiliate
    type: boolean
  - name: broadcastIsPartner
    description: Boolean value indicating if the broadcaster account is a Twitch partner
    type: boolean
  - name: broadcasterProfileUrl
    description: link to the 300x300px PNG version of a user's twitch profile image
    type: string
  - name: broadcasterOfflineUrl
    description: link to the 1920x1080px PNG version of a user's twitch
    type: string
  - name: broadcasterCreatedAt
    description: Datetime of when the account was created
    type: datetime
  - name: broadcasterDescription
    description: The user's channel description
    type: string
---

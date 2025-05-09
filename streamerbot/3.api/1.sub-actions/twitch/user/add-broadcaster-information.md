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
    description: Link to the 300x300px PNG version of the broadcaster's Twitch profile image
    type: string
  - name: broadcasterOfflineUrl
    description: Link to the 1920×1080 PNG version of the broadcaster's Twitch offline banner
    type: string
  - name: broadcasterCreatedAt
    description: Datetime of when the account was created
    type: datetime
  - name: broadcasterDescription
    description: The user's channel description
    type: string
---

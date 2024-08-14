---
title: Gift Membership Received
description: Trigger for new YouTube gift memberships
variables:
  - name: id
    type: string
    description: The id of the membership gifting event
  - name: tier
    type: string
    description: The tier the gifted user received
  - name: gifterUser
    type: string
    description: The display name of the user who gave the gifted membership
  - name: gifterUserName
    type: string
    description: The user name of the user who gave the gifted membership
  - name: gifterUserId
    type: string
    description: The id of the user who gave the gifted membership
  - name: gifterUserType
    type: string
    description: The type of user who gave the gifted membership
  - name: gifterProfileUrl
    type: string
    description: The profile image of the user who gave the gifted membership
  - name: gifterIsSponsor
    type: string
    description: Indicates whether the user who gave the gifted membership is a current channel member or not
commonVariables:
  - YouTubeUser
  - YouTubeBroadcast
  - YouTubeBroadcaster
---

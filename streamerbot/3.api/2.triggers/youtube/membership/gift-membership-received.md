---
title: Gift Membership Received
description: Trigger for new YouTube gift memberships
variables:
  - name: id
    type: string
    description: The id of the membership gifting event
  - name: tier
    type: number
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
commonVariables:
  - YouTubeUser
  - YouTubeBroadcaster
---

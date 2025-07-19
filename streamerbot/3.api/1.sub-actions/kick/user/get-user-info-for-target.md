---
title: Kick Add Target Info
description: Fetch Kick user data and populate a set of variables
variables:
  - name: targetUser
    description: Display name of the target user
  - name: targetUserName
    description: User name of the target user
  - name: targetUserId
    description: User Id of the target user
  - name: targetDescription
    description: The user's channel description
  - name: targetDescriptionEscaped
    description: The user's channel description but URL encoded
  - name: targetUserProfileImageUrl
    description: link to the 300x300px PNG version of a user's twitch profile image
  - name: targetUserProfileImageUrlEscaped
    description: The url to the user's profile image URL encoded
  - name: targetUserType
    description: The type of user, `affiliate`, `partner` or empty for regular user
---

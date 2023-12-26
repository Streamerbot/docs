---
title: Twitch User Variables
navigation.title: Twitch User
variables:
  - name: user
    type: string
    description: The display name of the user
    value: TwitchUser123
  - name: userName
    type: string
    description: The login name of the user
    value: twitchuser123
  - name: userId
    type: string
    description: Unique user identifier
    value: a126e8a8-43f7-4a14-8990-e8c3feea76d8
  - name: userType
    type: string
    description: Streaming service of this user
    value: twitch
  - name: isSubscribed
    type: boolean
    description: Is this user subscribed?
    value: True
  - name: isModerator
    type: boolean
    description: Is this user a moderator?
    value: True
  - name: isVip
    type: boolean
    description: Is this user a VIP?
    value: True
  - name: userPreviousActive
    type: DateTime
    description: When was this user last active?
    value: 8/4/2023 10:56:06 AM
  - name: badges
    type: List<TwitchBadge>
    description: A C# accessible list of emotes used in the chat message
    variables:
      - name: name
        type: string
        description: The name of the badge
        value: moderator
      - name: version
        type: number
        description: The version of the badge
        value: 1
      - name: imageUrl
        type: string
        description: The image URL of the badge
        value: https://static-cdn.jtvnw.net/badges/v1/3267646d-33f0-4b17-b3df-f923a41db1d0/3
  - name: badgeCount
    type: number
    description: The count of badges this user has
    value: 3
---
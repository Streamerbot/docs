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
    value: 718933593
  - name: userType
    type: string
    description: Streaming service of this user
    value: twitch
  - name: userGroups
    version: 0.2.5
    type: string
    description: Comma-delimited list of groups the user is in
    value: Awesome Streamers,Discord Peeps,Top Contributors
  - name: isSubscribed
    type: boolean
    description: Is this user subscribed?
    value: True
  - name: subscriptionTier
    type: number
    description: The subscription tier (T1 = 1000, T2 = 2000, T3 = 3000) (only available if `isSubscribed` is `True`)
    value: 3000
  - name: monthsSubscribed
    type: number
    description: The amount of months the user is subscribed
    value: 3
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
    type: List<Twitch.Common.Models.Badge>
    description: A C# accessible list of emotes used in the chat message
    children:
      - name: Name
        type: string
        description: The name of the badge
        value: moderator
      - name: Version
        type: number
        description: The version of the badge
        value: 1
      - name: ImageUrl
        type: string
        description: The image URL of the badge
        value: https://static-cdn.jtvnw.net/badges/v1/3267646d-33f0-4b17-b3df-f923a41db1d0/3
  - name: badgeCount
    type: number
    description: The count of badges this user has
    value: 3
---

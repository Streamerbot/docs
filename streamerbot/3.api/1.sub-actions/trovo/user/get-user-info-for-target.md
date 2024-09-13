---
title: Get User Info for Target
description: Fetch Trovo user data and populate a set of variables
commonVariables:
  - TrovoUser
parameters:
  - name: Source Type
    type: Select
    required: true
    description: |
      - `Broadcaster` - The currently logged in broadcaster account
      - `User` - User that invoked the action e.g. a raid leader, subscriber, point redeemer etc.
      - `From Input` - This will take the next word proceeding the trigger as the username to lookup. This user does not have to be present in the channel
      - `Variable` - Use the current value of an existing variable as the target
  - name: Variable
    type: string
    description: If you selected `Variable` as your `Source Type`, enter the name of the variable you would like to read in
variables:
  - name: targetUser
    type: string
    description: Display name of the target user
  - name: targetUserName
    type: string
    description: User name of the target user
  - name: targetUserId
    type: string
    description: User Id of the target user
  - name: targetUserPlatform
    type: string
    description: User platform of the target user
    value: trovo
  - name: targetInfo
    type: string
    description: Profile information of the target user
  - name: targetInfoEscaped
    type: string
    description: URL encoded profile information of the target user
  - name: targetUserProfileImageUrl
    type: string
    description: A link to the user's Trovo profile image
  - name: targetUserProfileImageUrlEscaped
    type: string
    description: The url to the user's profile image URL encoded
  - name: targetUserAudienceType
    type: string
    description: |
      The audience type the user caters to, it can be one of the following:
      
      - `CHANNEL_AUDIENCE_TYPE_FAMILYFRIENDLY`
      - `CHANNEL_AUDIENCE_TYPE_TEEN`
      - `CHANNEL_AUDIENCE_TYPE_EIGHTEENPLUS`
  - name: targetUserLanguage
    type: string
    description: Language of the channel, ISO2 format (2 letter language code)
    value: en
  - name: targetUserFolowers
    type: string
    description: The number of followers the target user has
  - name: targetLastActive
    type: string
    description: When the user was last active
  - name: targetPreviousActive
    type: string
    description: When the user was previously active
  - name: targetIsSubscribed
    type: boolean
    description: A boolean value indicating if the user is currently subscribed
  - name: targetSubscriptionTier
    type: string
    description: The tier at which the user is subscribed
  - name: targetIsModerator
    type: boolean
    description: Whether or not the target user is a moderator
  - name: liveTitle
    type: string
    description: If the user is currently live, this will contain the target user's live stream title
  - name: createdAt
    type: DateTime
    description: Datetime of when the target user's account was created
  - name: lastStreamTime
    type: DateTime
    description: Datetime of when the target user last streamed at
  - name: categoryName
    type: string
    description: The target user's current game category
  - name: categoryId
    type: string
    description: The numeric id of the game category
  - name: targetChannelTitle
    type: string
    description: The target user's channel title
---

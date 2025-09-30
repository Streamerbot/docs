---
title: Get User Info for Target
description: Fetch Twitch user data from a given value and populate a set of variables
variables:
  - name: addTargetResult
    type: bool
    description: Whether or not a user was found with the value that was used
    version: 1.0.0
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
  - name: targetIsAffiliate
    description: A boolean value indicating if the user is an affiliate
  - name: targetIsPartner
    description: A boolean value indicating if the user is a partner
  - name: targetLastActive
    description: When the user was last active
  - name: targetPreviousActive
    description: When the user was previously active
  - name: targetIsSubscribed
    description: A boolean value indicating if the user is currently subscribed
  - name: targetSubscriptionTier
    description: '`1000`, `2000`, `3000` - Numeric value indicating tier'
  - name: targetIsModerator
    description: A boolean value indicating if the user is a moderator
  - name: targetIsVip
    description: A boolean value indicating if the user is a VIP
  - name: targetChannelTitle
    description: The stream title of the user
  - name: game
    description: The user's current game category
  - name: gameId
    description: The numeric id of the game category
  - name: createdAt
    description: Datetime of when the account was created
  - name: accountAge
    description: Age of the account in seconds
  - name: tagCount
    description: A count of the tags that channel set most recently
  - name: tag#
    description: Consecutive arguments populated with one tag value each
  - name: tags
    description: All tags in a `list` format
  - name: tagsDelimited
    description: A comma separated list of all tags
---

## Parameters
::field{name="User Login" type=Text}
The User Login field can contain either a literal username or a variable/argument.
**Examples**
- `%userName%` – The user who triggered the action
- `genericuser` – A specific account with the name `genericuser`
- `%input0%` – The first input provided (e.g., in a command or reward)
- `%broadcastUserName` – The broadcaster’s account. If not used with a Twitch/Command trigger, be sure to add the [Add Broadcaster Information](/api/sub-actions/twitch/user/add-broadcaster-information) sub-action first
::
---
version: 0.1.14
---

# Shoutout Created
This triggers when a shoutout gets created in your chat.

## Details
::list
- Twitch Service: `Chat Client`
::

## Variables
:variables-description

Name | Description
----:|:------------
`shoutoutId` | Twitch's internal ID for the shoutout
`targetUserId` | The user's id
`targetUserLogin` | The user's login name
`targetUserDisplayName` | The user's display name
`targetUserPrimaryColorHex` | The user's primary color in hex
`targetUserProfileImageURL` | The user's profile image

User: Who created the shoutout
Target: Who reveived the shoutout

:variables{name=TwitchUser disclosure}

::wip
TODO: Add shared twitch target vars here
::
# User Timed Out
When a user gets timed out in chat.

## Details
::list
- Twitch Service: `PubSub`
::

## Variables
:variables-description
Name | Description
----:|:------------
`user` | The user who was timed out
`createdAt` | The timestamp when the timeout was created
`createdById` | The Twitch user id from who created the timeout 
`createdByUsername` | The user name from who created the timeout
`createdByDisplayName` | The display name from who created the timeout
`reason` | The reason for the timeout
`duration` | The duration of this timeout in seconds
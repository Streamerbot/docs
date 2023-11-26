# User Banned
When a user gets banned in chat.

## Details
::list
- Twitch Service: `PubSub`
::

## Variables
:variables-description
Name | Description
----:|:------------
`user` | The user who was banned <br> <small>*This will only be populated if the user has been present in chat*</small>
`createdAt` | The timestamp when the ban was created
`createdById` | The Twitch user id from who created the ban 
`createdByUsername` | The user name from who created the ban
`createdByDisplayName` | The display name from who created the ban
`reason` | The reason for the ban
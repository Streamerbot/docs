# Timeout User
Timeout a user.
:image-preview

## Parameters
### `Type`
Select who you want to timeout.

- `Redeemer`: Timeout the user who redeemed something e.g. a command or a channel point
- `Random`: Use a random user from your chat
- `Specific User`: Select a user from the known user list
- `From Input`: Use a value from an input like a command or a channel point reward

### `Specific User`
When you have selected the `Type` to `Specific User` you will be able to select a user from this list.

- Type: `Select`

### `Duration`
The duration the timeout should last.

- Type: `Integer`

### `Reason`
Enter the reason for the timeout.

- Type: `String`

### `Exclude Moderators`
Select this is you want to exclude moderators from the timeout.

- Type: `Checkbox`

## Variables
:variables-description

Name | Description
----:|:------------
`createdAt` | The timestamp the timeout was created.
`createdById` | User id from the timeout creator.
`createdByUsername` | User's login name from the timeout creator.
`createdByDisplayName` | Display name from the timeout creator.
`duration` | The duration of the timeout.
`reason` | The reason of the timeout

## C# Usage
:csharp-method{name=TwitchTimeoutUser}
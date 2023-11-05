# Get Follow Age Info for Target
Get the follow age from a Twitch user
:image-preview{width=400}

## Parameters
### `Source Type`
Select from which source you want to get the follow age:
- `User`: User that invoked the action e.g. a raid leader, subscriber, point redeemer etc.
- `From Input`: This will take the next word proceeding the trigger as the username to lookup. This user does not have to be present in the channel
- `Variable`: Use the content of an existing variable as the target

### `Variable`
If you selected `Variable` as your `Source Type`, enter the name of the variable you would like to read in.

## Variables
Name | Description
----:|:------------
`followDate`| The date the user followed
`followAgeLong` | How long the user has been following in a long format, 1 year, 10 months, 5 days, etc
`followAgeShort` | How long the user has been following in a short format, 1y, 10m, 5d, 22h, 3m, 25s
`followAgeDays` | The total number of days the user has been following
`followAgeMinutes` | The total number of minutes the user has been following
`followAgeSeconds` | The total number of seconds the user has been following
`followUser` | The users display name
`followUserName` | The user's login name
`followUserId` | The user's Twitch id

## C# Usage
:csharp-method
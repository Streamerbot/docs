# Add VIP
Add a VIP to your Twitch channel.
:image-preview

## Parameters
### `Source Type`
Select from which source you want to add a VIP:
- `User`: User that invoked the action e.g. a raid leader, subscriber, point redeemer etc.
- `From Input`: This will take the next word proceeding the trigger as the username to lookup. This user does not have to be present in the channel
- `Variable`: Use the content of an existing variable as the target

### `Variable`
If you selected `Variable` as your `Source Type`, enter the name of the variable you would like to read in.

## Variables
:variables-description{empty}

## C# Usage
:csharp-method{name=TwitchAddVip}
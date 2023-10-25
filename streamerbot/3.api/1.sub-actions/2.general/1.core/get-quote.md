# Get Quote
Fetch stored quotes for usage in subsequent sub-actions
:image-preview

## Parameters
### `Type`
The type can either be `Random` or `Specific`, if `Random`, a random quote will be picked from your available quotes, and added to the arguments

### `Quote Id`
Available when you have the `Type` set to `Specific`, you can specify the exact quote number to be added to the arguments

## Variables
:variables-description
Name | Description | Example
----:|:------------|---------|
`quoteTime` | The time that the quote was made
`quoteId` | The numeric id of the quote | `4219`
`quoteUserId` | The user id from the account that made the quote | `streamerbot`
`quoteUser` | The user's display name from the account that made the quote | `StreamerBot`
`quotePlatform` | The platform from the account that made the quote | `twitch`
`quoteGameId` | The game id from the quote `123942`
`quoteGame` | The game name from the quote | `Beat Saber`
`quote` | The quote itself | `this is a quote!`
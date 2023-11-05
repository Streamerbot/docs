# Update Redemption Status
Set a reward redemption as fulfilled or canceled.
:image-preview

::callout{icon=i-mdi-bookmark color=green}
A redeem must be originally created by Streamer.bot for this sub-action to work.
::

## Parameters
### `Status`
- `Fulfilled`: Accept the redemption, marking it as complete
- `Cancel`: Cancel the reward redemption, refunding any channel points spent

## Variables
:variables-description{empty}

## C# Usage
:csharp-method{name=TwitchRedemptionFulfill}
:csharp-method{name=TwitchRedemptionCancel}
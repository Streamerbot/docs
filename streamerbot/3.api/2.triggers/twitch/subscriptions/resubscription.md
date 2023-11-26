# Resubscription
This triggers when you get a resubscription.

## Details
::list
- Twitch Service: `Chat Client`
::

## Variables
:variables-description

Name | Descriptions
----:|:------------
`tier` | Subscription tier <br> `prime`, `tier 1`. `tier 2`, `tier 3`
`monthStreak` | Current subscription streak in months.
`cumulative` | Total number of months a user has been subscribed for
`rawInput` | The message entered.
`rawInputEscaped` | The message escaped
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`color` | User's color (if they have chosen one or a random one if not)

:variables{name=TwitchUser disclosure}
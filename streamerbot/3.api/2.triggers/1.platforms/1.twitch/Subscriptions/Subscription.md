# Subscription
This triggers when you get a subscription.

## Details
::list
- Twitch Service: `Chat Client`
::

## Variables
:variables-description

Name | Description
----:|:------------
`tier` | Subscription tier <br> `prime`, `tier 1`. `tier 2`, `tier 3`
`rawInput` | The message entered
`rawInputEscaped` | The message escaped
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`color` | User's color (if they have chosen one or a random one if not)

:variables{name=TwitchUser disclosure}
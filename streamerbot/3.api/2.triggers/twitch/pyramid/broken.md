# Pyramid Broken
This triggers when a pyramid gets destroyed in Twitch chat.

## Details
::list
- Twitch Service: `Chat Client`
::

## Variables
:variables-description

Name | Description
----:|:------------
`totalPyramidsBroken` | The total amount of pyramids the user has broken.
`pyramidWidth` | The total amount of pyramid layers.
`pyramidEmote` | The emote that was used in the pyramid.
`pyramidOwnerId` | The user id of the person who intiated the pyramid.
`pyramidOwnerUsername` | The user name of the person who intiated the pyramid.
`pyramidOwnerDisplayName` | The user display of the person who intiated the pyramid.

::callout{color=amber icon=i-mdi-lightbulb}
The user variables are for the person who destroyed the pyramid.
::

:variables{name=TwitchUser disclosure}
# Gift Bomb
This triggers when someone does a gift bomb.

## Details
::list
- Twitch Service: `Chat Client`
::

## Variables
:variables-description

Name | Description
----:|:------------
`gifts` | Number of subscriptions in this gift bomb
`totalGifts` | Total number of subscriptions this user has gifted
`fromGiftBomb` | Boolean value if sub came from a gift bomb <br>  `True`/`False` 
`anonymous` | Boolean value indicating the gift was anonymous <br> `True`/`False` 
`tier` | The subscriptions tier <br> `tier 1`. `tier 2`, `tier 3`

:variables{name=TwitchUser disclosure}
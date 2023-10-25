# Tip
StreamElements tip trigger.

## Details
This event triggers when you get a tip with StreamElements.

## Parameters
### `Range`
:range-description

## Variables
:variables-description

Name | Description
----:|:------------
`tipUsername` | Username of the user as provided by StreamElements (may not be from Twitch)
`tipAvatar` | The URL of the user's avatar
`tipAmount` | The amount of the tip
`tipCurrency` | The 3 letter payment currency code
`tipMessage` | The tip message that the user may has included
`isTest` | Boolean value indicating if the tip was a test `True`/`False`
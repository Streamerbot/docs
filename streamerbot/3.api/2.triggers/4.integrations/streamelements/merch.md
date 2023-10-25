# Merch
Streamlabs merch trigger.

## Details
This event triggers when you someone buys merch in your Streamlabs store.

## Variables
:variables-description

Name | Description
----:|:------------
`merchUsername` | Username of the user as provided by StreamElements (may not be from Twitch)
`merchAvatar` | The URL of the user's avatar
`merchAmount` | The amount of the purchase
`merchCurrency` | The 3 letter payment currency code
`merchMessage` | The message that the user may has included
`merchQuantity` | The total number of items purchased
`merchItems` | The number of distinct items purchased
`merchItem#.name` | Name of the item purchased, where # is the index of the item (0 based)
`merchItem#.price` | Price of the item purchased, where # is the index of the item (0 based)
`merchItem#.quantity` | How many of the item was purchased, where # is the index of the item (0 based)
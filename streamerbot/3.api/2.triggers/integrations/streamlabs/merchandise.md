# Merchandise
Streamlabs merchandise trigger.

## Details
This event triggers when you someone buys merchandise in your Streamlabs store.

## Variables
:variables-description

Name | Description
----:|:------------
`merchandiseFrom` | Username of the user as provided by Streamlabs (may not be from Twitch)
`merchandiseMessage` | The message that the user may has included
`merchandiseProduct` | The product that was purchased
`merchandiseImageUrl` | The URL to the image of the product
`merchandiseImageEscaped` | The URL to the image of the product with escaped characters
`isTest` | Boolean value indicating if the tip was a test `True`/`False`
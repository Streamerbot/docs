# Donation
Ko-Fi shop order trigger.

## Details
This event triggers when someone makes a shop order in Ko-Fi.

## Variables
:variables-description

Name | Description
----:|:------------
`messageId` | Kofi's internal ID
`timestamp` | Timestamp of when the event occured
`from` | Username of who triggered the event
`isPublic` | Whether or not the message is shared publicly `True`/`False`
`message` | Message the user left
`amount` | The order amount
`currency` | The currency of the order
`itemCount` | The currency of the donation
`item#` | The id of the item purchased, where # is the index of the item
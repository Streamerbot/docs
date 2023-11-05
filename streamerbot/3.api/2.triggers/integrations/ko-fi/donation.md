# Donation
Ko-Fi donation trigger.

## Details
This event triggers when you get a donation in Ko-Fi.

## Variables
:variables-description

Name | Description
----:|:------------
`messageId` | Kofi's internal ID
`timestamp` | Timestamp of when the event occured
`from` | Username of who triggered the event
`isPublic` | Whether or not the message is shared publicly `True`/`False`
`message` | Message the user left
`amount` | The donation amount
`currency` | The currency of the donation
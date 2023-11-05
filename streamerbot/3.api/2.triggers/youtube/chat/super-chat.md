# Super Chat

## Variables
:variables-description
Name | Description
----:|:------------
`messageId` | The id of the super chat event
`message` | The message of the super chat event
`publishedAt` | The time the super chat event was published at
`tier` | The tier for the paid message
`amount` | A string, like $1.00, that contains the purchase amount and currency. The string is intended to be displayed to the user.
`microAmount` | The purchase amount, in micros of the purchase currency. For example, if the purchase amount is one dollar, the value is `1000000`.
`currencyCode` | The currency in which the purchase was made. The value is an ISO 4217 currency code.
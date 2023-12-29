# Donation
Streamlabs donation trigger.

## Details
This event triggers when you get a donation with Streamlabs.

## Parameters
### `Range`
:range-description

## Variables
:variables-description

Name | Description
----:|:------------
`donationFrom` | Username of the user as provided by Streamlabs (may not be from Twitch)
`donationAmount` | The amount of the donation
`donationCurrency` | The 3 letter payment currency code
`donationFormattedAmount` | The donation amount with the currency symbol
`donationMessage` | The donation message that the user may has included
`isTest` | Boolean value indicating if the tip was a test `True`/`False`
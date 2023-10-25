---
version: 0.1.14
---

# Charity Donation
When a charity event gets a donation.

## Details
::list
- Twitch Service: `EventSub`
::

## Variables
:variables-description
Name | Description
----:|:------------
`charity.amount.value` | The amount of the donation in decimal form e.g. `5.25` ($5.25).
`charity.amount.valueMinor` | The amount of the donation in non-decimal form e.g. `525` ($5.25).
`charity.amount.currency` | The 3 letter ISO currency code.
`charity.campaignId` | Twitch's internal ID for your campaign.
`charity.name` | The name of the charity you're supporting.
`charity.description` | The description of the charity you're supporting.
`charity.logo` | The URL to the logo of the charity you're supporting.
`charity.website` | The URL to the website of the charity you're supporting.
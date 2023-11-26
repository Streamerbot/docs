---
version: 0.1.15
---

# Charity Started
When a charity event starts.

## Details
::list
- Twitch Service: `EventSub`
::

## Variables
:variables-description
Name | Description
----:|:------------
`charity.startedAt` | The time and date the charity event started, format: `MM/dd/yyyy h:m:ss tt`.
`charity.currentAmount.value` | The current amount of the money raised in decimal form e.g. `5.25` ($5.25).
`charity.currentAmount.valueMinor` | The current amount of the money raised in non-decimal form e.g. `525` ($5.25).
`charity.currentAmount.currency` | The 3 letter ISO currency code for the current amount of money raised.
`charity.targetAmount.value` | The target amount of the money to be raised in decimal form e.g. `20` ($20.00).
`charity.targetAmount.valueMinor` | The target amount of the money to be raised in non-decimal form e.g. `2000` ($20.00).
`charity.targetAmount.currency` | The 3 letter ISO currency code for the target amount of money to be raised.
`charity.id` | Twitch's internal ID for your campaign.
`charity.name` | The name of the charity you're supporting.
`charity.description` | The description of the charity you're supporting.
`charity.logo` | The URL to the logo of the charity you're supporting.
`charity.website` | The URL to the website of the charity you're supporting.
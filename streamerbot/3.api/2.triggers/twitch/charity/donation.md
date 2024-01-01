---
title: Charity Donation
description: Trigger for the Twitch charity donation event
version: 0.1.14
twitchService: EventSub
variables:
  - name: charity.amount.value
    type: number
    description: The donation amount
    value: 5.25
  - name: charity.amount.valueMinor
    type: number
    description: The donation amount in the minor format
    value: 525
  - name: charity.amount.currency
    type: string
    description: The currency formatted in the 3 letter ISO currency code of the donation
    value: USD
  - name: charity.campaignId
    type: string
    description: The unique identifier for the charity campaign
  - name: charity.name
    type: string
    description: The name of the charity campaign
    value: My charity campaign
  - name: charity.description
    type: string
    description: The description of the charity campaign
    value: My charity campaign description
  - name: charity.logo
    type: string
    description: The image url of the logo from the charity campaign
  - name: charity.website
    type: string
    description: The website of the charity campaign
    value: mycharitycampaign.com
---

## Parameters
::field-group
  ::field{name=Range type=Range}
    :range-description
  ::
::
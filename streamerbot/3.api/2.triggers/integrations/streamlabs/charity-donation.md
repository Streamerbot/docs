---
title: Charity Donation
description: Trigger for when a charity donation occurs through Streamlabs
version: 0.2.3
parameters:
  - name: Range
    import: common/range
variables:
  - name: charityDonationFrom
    type: string
    description: The username of the user as provided by Streamlabs (may not be from Twitch)
  - name: charityDonationAmount
    type: number
    description: The amount of the charity donation
    value: 5
  - name: charityDonationCurrency
    type: string
    description: The 3 letter payment currency code
    value: EUR
  - name: charityDonationFormattedAmount
    type: string
    description: The charity donation amount with the currency symbol
    value: €5
  - name: charityDonationMessage
    type: string
    description: The charity donation message that the user may have included
    value: My donation message
  - name: charityDonationGif
    type: string
    description: A GIF that the user may have included
  - name: charityDonationIconClassName
    type: string
  - name: charityDonationCreatedAt
    type: DateTime
    description: The date and time the charity donation was made
---

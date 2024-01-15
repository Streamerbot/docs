---
title: Donation
description: Trigger for a Streamlabs Donation
variables:
  - name: donationFrom
    type: string
    description: The username of the user as provided by Streamlabs (may not be from Twitch)
  - name: donationAmount
    type: number
    description: The amount of the donation
    value: 5
  - name: donationCurrency
    type: string
    description: The 3 letter payment currency code
    value: EUR
  - name: donationFormattedAmount
    type: string
    description: The donation amount with the currency symbol
    value: €5
  - name: donationMessage
    type: string
    description: The donation message that the user may has included
    value: My donation message
---

## Parameters
::field-group
  ::field{name=Range type=Range}
    :range-description
  ::
::
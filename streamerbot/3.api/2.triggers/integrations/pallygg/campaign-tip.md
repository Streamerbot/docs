---
title: Campaign Tip
description: Trigger for when a tip has been received
version: 0.2.4
parameters:
  - name: Range
variables:
  - name: tipId
    type: string
    description: The ID of the tip on Pally.gg
  - name: tipDisplayName
    type: string
    description: The name used for the tip
  - name: tipNetAmount
    type: decimal
    description: The amount of the tip that you will receive
    value: 1.0
  - name: tipNetAmountInCents
    type: int
    description: The amount of the tip that you will receive in cents
    value: 100
  - name: tipNetAmountFormatted
    type: string
    description: The amount of the tip that you will receive, formatted as a string with currency symbol
    value: '$1.00'
  - name: tipMessage
    type: string
    description: If provided, the message that was sent along with the tip
  - name: tipGrossAmount
    type: decimal
    description: The total amount of the tip
    value: 1.25
  - name: tipGrossAmountInCents
    type: int
    description: The total amount of the tip, in cents
    value: 125
  - name: tipGrossAmountFormatted
    description: The total amount of the tip, formatted as a string with currency symbol
    value: '$1.25'
    type: string
  - name: tipProccessingFee
    type: decimal
    description: The processing fee for the tip
    value: 0.25
  - name: tipProccessingFeeInCents
    type: int
    description: The processing fee for the tip, in cents
    value: 25
  - name: tipProccessingFeeFormatted
    type: string
    description: The processing fee for the tip, formatted as a string with currency symbol
    value: '$0.25'
  - name: createdAt
    type: DateTime
    description: When the tip was given
  - name: campaignId
    type: string
    description: The ID of the campaign at Pally.gg
  - name: campaignTitle
    type: string
    description: The title of the campaign at Pally.gg
  - name: campaignSlug
    type: string
    description: The URL slug of the campaign
  - name: campaignUrl
    type: string
    description: The URL of the campaign
---

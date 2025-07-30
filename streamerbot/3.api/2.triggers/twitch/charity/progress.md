---
title: Charity Progress
description: Trigger for the Twitch charity progress event
version: 0.1.15
twitchService: EventSub
variables:
  - name: charity.currentAmount.value
    type: number
    description: The current amount of money raised
    value: 5.25
  - name: charity.currentAmount.valueMinor
    type: number
    description: The current amount of money raised in the minor format
    value: 525
  - name: charity.currentAmount.currency
    type: string
    description: The currency formatted in the 3 letter ISO currency code of the amount raised
    value: USD
  - name: charity.targetAmount.value
    type: number
    description: The target amount of money raised
    value: 20
  - name: charity.targetAmount.valueMinor
    type: number
    description: The target amount of money raised in the minor format
    value: 2000
  - name: charity.targetAmount.currency
    type: string
    description: The currency formatted in the 3 letter ISO currency code of the target amount raised
    value: USD
  - name: charity.id
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
commonVariables:
  - TwitchBroadcaster
---

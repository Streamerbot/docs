---
title: Donation
description: Trigger for a FourthWall Donation
version: 0.2.3
variables:
  - name: fw.createdAt
    type: DateTime
    description: The DateTime of the donation in UTC
  - name: fw.donationId
    type: string
    description: Id of the donation
  - name: fw.shopId
    type: string
    description: Id of the shop
    value: sh_7ad0c438-beda-4779-a885-0dc325a755c1
  - name: fw.username
    type: string
    description: Username of the supporter
  - name: fw.email
    type: string
    description: E-mail adress of the supporter
    value: support@fourthwall.com
  - name: fw.message
    type: string
    description: Attached message
    value: message from supporter
  - name: fw.amount
    type: number
    description: Amount of donation
    value: 5
  - name: fw.currency
    type: string
    description: Donation currency
    value: USD
  - name: fw.status
    type: string
    description: Status of the donation
    value: COMPLETED
---

## Parameters
### `Range`
:range-description
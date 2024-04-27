---
title: Subscription Expired
description: Trigger for a FourthWall subscription expiring
version: 0.2.3
variables:
  - name: fw.createdAt
    type: DateTime
    description: The DateTime of subscription change
  - name: fw.id
    type: string
    description: Id of the subscription
    value: SupporterId(value=7ad0c438-beda-4779-a885-0dc325a755c1)
  - name: fw.shopId
    type: string
    description: Id of the shop
    value: sh_7ad0c438-beda-4779-a885-0dc325a755c1
  - name: fw.nickname
    type: string
    description: Username
  - name: fw.email
    type: string
    description: E-mail adress
    value: support@fourthwall.com
  - name: fw.amount
    type: number
    description: Amount
    value: 5
  - name: fw.currency
    type: string
    description: Currency
    value: USD
  - name: fw.interval
    type: string
    description: Interval of subscription
    value: MONTHLY
  - name: fw.type
    type: string
    description: Type of change
    value: CANCELLED
---
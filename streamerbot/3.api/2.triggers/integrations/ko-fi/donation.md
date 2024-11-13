---
title: Donation
description: Trigger for a Ko-Fi Donation
version: 0.1.8
parameters:
  - name: Range
variables:
  - name: messageId
    type: string
    description: Kofi's internal identifier
  - name: timestamp
    type: DateTime
    description: The timestamp of the event
    value: 8/4/2023 10:56:06 AM
  - name: from
    type: string
    description: The username from who triggered the event
    value: KoFiUser123
  - name: isPublic
    type: boolean
    description: Is the message shared publicly?
    value: True
  - name: message
    type: string
    description: The message the user left
    value: My Ko-Fi message
  - name: amount
    type: number
    description: The donation amount
    value: 10
  - name: currency
    type: string
    description: The currency of the donation
    value: EUR
---

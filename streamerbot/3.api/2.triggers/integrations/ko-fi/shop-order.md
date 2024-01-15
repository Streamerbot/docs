---
title: Shop Order
description: Trigger for a Ko-Fi Shop Order
version: 0.1.8
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
    description: The order amount
    value: 10
  - name: currency
    type: string
    description: The currency of the order
    value: EUR
  - name: itemCount
    type: number
    description: The amount of items
    value: 5
  - name: item#
    type: string
    description: The id of the item purchased
---
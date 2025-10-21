---
title: Donation
description: Trigger for a TipeeeStream Donation
version: 0.1.8
parameters:
  - name: Range
    import: common/range
variables:
  - name: tipeeStreamId
    type: string
    description: The id from TipeeeStream
  - name: timestamp
    type: DateTime
    description: The timestamp of this event
    value: 8/4/2023 10:56:06 AM
  - name: username
    type: string
    description: Who the donation was from, as the user filled out
    value: TipeeeStreamUser123
  - name: avatar
    type: string
    description: Avatar of the user
  - name: amount
    type: number
    description: The amount of the tip (decimal value)
    value: 5
  - name: fees
    type: number
    description: The fees that will be taken from the tip
    value: 0.2
  - name: currency
    type: string
    description: The 3 letter currency code
    value: EUR
  - name: message
    type: string
    description: Any donation message the user may have included
    value: My donation message
---

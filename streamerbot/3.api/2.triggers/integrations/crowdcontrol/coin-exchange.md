---
title: Coin Exchange
description: When a CrowdControl user exchanges for CrowdControl's Coin currency
parameters:
  - name: Coin Type
    type: Select
    required: true
    default: Any
    description: |
      - `Any`
      - `Free`
      - `Paid`
  - name: Exchange Source
    type: Select
    required: true
    default: Any
    description: |
      - `Any`
      - `Paypal`
      - `Stripe`
      - `Tiltify`
      - `Twitch Bits`/`Twitch Channel Points`/`Twitch Sub`
  - name: Amount
    type: Range
    description: |
      Filter events between a specified `Min` and `Max`

      `Min` and `Max` are **inclusive** of the entered values

      - `Any Value` - Leave both min and max empty to accept any value
      - `Exact Value` - Enter only a `Max` to trigger on a specific value
      - `Greater Than` - Enter only a `Min` to trigger on any value greater than the specified value
      - `Range` - Enter a min and a max to trigger within a desired range
variables:
  - name: coinType
    type: string
    description: The type 
    value: free
  - name: exchangeSource
    type: string
    description: The source of the exchange
    value: twitch-sub
  - name: anonymous
    type: bool
    description: If it was an anoymous exchange
    value: False
  - name: bonus
    type: int
    description: Amount of bonus coins
    value: 0
---
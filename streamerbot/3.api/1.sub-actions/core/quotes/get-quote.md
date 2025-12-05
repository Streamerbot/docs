---
title: Get Quote
description: Fetch stored quotes for usage in subsequent sub-actions
parameters:
  - name: Type
    type: Select
    required: true
    default: Random
    options:
      - value: Random
        description: Fetch a random quote from your stored quotes
      - value: Specific
        description: Fetch a specific quote by its ID
  - name: Quote Id
    type: Number
    required: false
    description: The specific quote ID to fetch, only used if `Type` is set to `Specific`
variables:
  - name: quoteTimestamp
    type: DateTime
    description: |
      The date and time that the quote was made.  Can be formatted with `DateTime` format strings.
      ::read-more{to=/guide/variables#date-and-time}
        Read more about date and time format strings
      ::
    value: 1/29/2022 12:00:00 AM
  - name: quoteTime
    type: string
    description: The date that the quote was made, formatted in accordance with your computer's "Short date" format setting
    value: 10/17/2025
  - name: quoteId
    type: string
    description: The numeric id of the quote
    value: '4219'
  - name: quoteUserId
    type: string
    description: The user id from the account that made the quote
    value: '12345678'
  - name: quoteUser
    type: string
    description: The user's display name from the account that made the quote
    value: StreamerBot
  - name: quotePlatform
    type: string
    description: The platform from the account that made the quote
    value: twitch
  - name: quoteGame
    type: string
    description: The game name from the quote
    value: Beat Saber
  - name: quote
    type: string
    description: The quote itself
    value: This is a quote!
csharpMethods:
  - GetQuote
---

:read-more{to=/examples/quotes-commands}

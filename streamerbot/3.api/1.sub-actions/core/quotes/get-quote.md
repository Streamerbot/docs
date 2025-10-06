---
title: Get Quote
description: Fetch stored quotes for usage in subsequent sub-actions
parameters:
  - name: Type
    type: Select
    required: true
    default: Random
    options:
      - name: Random
        description: Fetch a random quote from your stored quotes
      - name: Specific
        description: Fetch a specific quote by its ID
  - name: Quote Id
    type: Number
    required: false
    description: The specific quote ID to fetch, only used if `Type` is set to `Specific`
variables:
  - name: quoteTime
    type: string
    description: The time that the quote was made
    value: 2024-01-01T12:00:00Z
  - name: quoteId
    type: string
    description: The numeric id of the quote
    value: '4219'
  - name: quoteUserId
    type: string
    description: The user id from the account that made the quote
    value: 'streamerbot'
  - name: quoteUser
    type: string
    description: The user's display name from the account that made the quote
    value: StreamerBot
  - name: quotePlatform
    type: string
    description: The platform from the account that made the quote
    value: twitch
  - name: quoteGameId
    type: string
    description: The game id from the quote
    value: '123942'
  - name: quoteGame
    type: string
    description: The game name from the quote
    value: Beat Saber
  - name: quote
    type: string
    description: The quote itself
    value: This is a quote!
---

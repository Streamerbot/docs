---
title: Add Quote
description: Add a quote which can be retrieved by the `Get Quote` Sub-Action
parameters:
  - name: Variable
    type: Text
    required: true
    description: The text of the quote to add.
variables:
  - name: success
    type: bool
    description: Whether the quote was added successfully
    value: true
  - name: quoteTime
    type: string
    description: The time that the quote was made
    value: 10/17/2025
  - name: quoteId
    type: string
    description: The numeric id of the quote which was just added
    value: '4219'
  - name: quoteUserId
    type: string
    description: The user id from the account that added the quote
    value: '12345678'
  - name: quoteUser
    type: string
    description: The user's display name from the account that added the quote
    value: StreamerBot
  - name: quotePlatform
    type: string
    description: The platform from the account that added the quote
    value: twitch
  - name: quoteGame
    type: string
    description: The category set on the channel when the quote was added
    value: Beat Saber
  - name: quote
    type: string
    description: The quote itself
    value: This is a quote!
csharpMethods:
  - AddQuoteForTwitch
  - AddQuoteForYouTube
  - AddQuoteForKick
  - AddQuoteForTrovo
---

::tip
This Sub-Action will set the quote user to the user who called the action<br/>
Setting the quote user to a different user than the caller is only supported via the C# Method
::

:read-more{to=examples/quotes-commands}
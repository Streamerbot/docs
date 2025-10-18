---
title: Get Quote Count
description: Get the total number of quotes
variables:
  - name: quoteCount
    type: number
    description: The total number of quotes which have been added.
    value: 250
csharpMethods:
  - GetQuoteCount
---

::tip
The Count returned by this Sub-Action is not necessarily the same as the last Quote ID, on account of deleted quotes.
::

:read-more{to=examples/quotes-commands}
---
title: Delete Quote
description: Delete the selected Quote
parameters:
  - name: Quote Id
    type: Number
    required: true
    description: The Quote ID to delete.
variables:
  - name: success
    type: bool
    description: Whether the quote was deleted successfully
    value: true
  - name: quoteId
    type: string
    description: If `success` is true, contains the numeric id of the quote which was just deleted
    value: '4219'
  - name: error
    type: string
    description: If `success` is false, contains the reason that deleting the quote failed
    value: Unable to delete quote 4219, it does not exist
csharpMethods:
  - DeleteQuote
---

![Get Quote Sub-Action](assets/get-quote.png)

::tip
Deleting a quote does not change the Quote ID of following quotes<br/>
You can Re-Index quotes manually under `Services > Quotes` by right-clicking and choosing `Re-index` from the context menu.  **This operation can not be undone**
::

:read-more{to=examples/quotes-commands}
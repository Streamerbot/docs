---
title: Item Set Value
description: Set the status value of an item in a Streamer.bot deck
version: 1.0.0
parameters:
  - name: Deck
    type: Select
    description: Select the deck where the item is located
    required: true
  - name: Item
    type: Select
    description: Select the item to modify
    required: true
  - name: Value
    type: Number
    description: Set the value for the item
  - name: State
    type: Number
    description: Apply the change to a specific state of the item (0 for default, 1 for active, etc.)
    default: 0
---

::note
[Streamer.bot Website Integration](/guide/integrations/streamerbot) is required for this sub-action
::

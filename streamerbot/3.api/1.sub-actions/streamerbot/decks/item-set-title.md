---
title: Item Set State
description: Set the active state of an item in a Streamer.bot deck
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
  - name: Title
    type: Text
    description: Set the title text for the item
  - name: Color
    type: Text
    description: Set an optional color for the title text (hex code or color name)
  - name: State
    type: Number
    description: Apply the change to a specific state of the item (0 for default, 1 for active, etc.)
    default: 0
---

::note
[Streamer.bot Website Integration](/guide/integrations/streamerbot) is required for this sub-action
::

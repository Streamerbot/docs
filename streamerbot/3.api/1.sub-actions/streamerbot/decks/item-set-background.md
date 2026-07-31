---
title: Item Set Background
description: Set the background of a specific item in a Streamer.bot deck
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
  - name: Color
    type: Text
    description: Set an optional background color for the item (hex code or color name)
  - name: URL
    type: Text
    description: Set an optional image URL for the item
  - name: File ID
    type: Text
    description: Set an optional image file ID for the item (for files uploaded to Streamer.bot)
  - name: State
    type: Number
    description: Apply the change to a specific state of the item (0 for default, 1 for active, etc.)
    default: 0
---

::note
[Streamer.bot Website Integration](/guide/integrations/streamerbot) is required for this sub-action
::

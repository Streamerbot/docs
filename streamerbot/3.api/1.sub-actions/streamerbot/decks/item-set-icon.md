---
title: Item Set Icon
description: Set the icon of a specific item in a Streamer.bot deck
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
    description: Set an optional color for the icon (hex code or color name)
  - name: Name
    type: Text
    description: Set the item's icon to an [Iconify](https://icon-sets.iconify.design/) icon name, e.g. 'mdi:home' or 'heroicons:arrow-left'
  - name: URL
    type: Text
    description: Set the item's icon to an image URL
  - name: File ID
    type: Text
    description: Set the item's icon to an image file ID (for files uploaded to Streamer.bot)
  - name: State
    type: Number
    description: Apply the change to a specific state of the item (0 for default, 1 for active, etc.)
    default: 0
---

::note
[Streamer.bot Website Integration](/guide/integrations/streamerbot) is required for this sub-action
::

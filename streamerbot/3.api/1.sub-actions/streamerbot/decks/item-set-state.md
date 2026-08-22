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
  - name: State
    type: Number
    description: Enter the state to make active for the selected item (0 for default, 1 for active, etc.)
    default: 0
---

::note
[Streamer.bot Website Integration](/guide/integrations/streamerbot) is required for this sub-action
::

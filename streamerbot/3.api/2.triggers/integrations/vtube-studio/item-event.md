---
title: Item Event
description: Triggers every time certain actions are done with/by an item
version: 0.2.3
variables:
  - name: itemEventType
    type: string
    description: The item event type
    value: Added, Removed, DroppedPinned, DroppedUnpinned, Clicked, Locked, Unlocked
  - name: itemInstanceId
    type: string
    description: The item's instance ID. If you pass in a list of item IDs, items with non-matching IDs will not trigger the event
    value: a27fa7a3c94c44d5a15c0abb4c3128a9
  - name: itemFileName
    type: string
    description: The item's file name. If you pass in a list of item filenames, items with non-matching filenames will not trigger the event. This does "contains-matching", so for example if you pass in "my", it will match the item my_item.png
    value: Black Sunglasses
  - name: position.x
    type: double
    description: The item x position in the usual coordinate system
    value: 0.0479986667633057
  - name: position.y
    type: double
    description: The item y position in the usual coordinate system
    value: 0.344514489173889
---

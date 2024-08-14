---
title: Item Hit
description: Trigger for when your character is hit by an item in T.I.T.S.
version: 0.2.3
variables:
  - name: itemId
    type: string
    description: The id of the item that hit
  - name: itemName
    type: string
    description: The friendly name of the item that hit
  - name: triggerId
    type: string
    description: The id of the trigger that caused the item hit
  - name: triggerName
    type: string
    description: the friendly name of the trigger that caused the item hit
  - name: strength
    type: double
  - name: direction.x
    type: double
  - name: direction.y
    type: double
  - name: direction.z
    type: double
---

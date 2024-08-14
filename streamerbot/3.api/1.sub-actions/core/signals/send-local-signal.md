---
title: Send Local Signal
description: Send a signal within the local instance of Streamer.bot
version: 0.2.4
parameters:
  - name: Signal Name
    type: String
    required: true
    description: Name of the signal
  - name: Include Action's Arguments
    type: Checkbox
    required: false
    description: Sends all the action's available arguments to the other instance
  - name: Arguments
    type: List
    required: false
    description: Sends the specified arguments over to the second instance. It's not affected by "Include Action's Arguments" and those arguments are always included.
  - name: Queue Signal
    type: boolean
    descripton: Whether or not to queue the signal that can be picked up by a Wait for Local Signal that has yet to happen
variables: []
csharpMethods: []
---

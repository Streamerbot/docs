---
title: Wait For Remote Signal
description: Wait for a remote signal from another Streamer.bot instance
version: 0.2.4
parameters:
  - name: Instance
    type: Selection
    required: true
    description: Select a specific instance or send it to any
  - name: Event Name
    type: String
    required: true
    description: Name of the event. The event names have to match for the trigger and the "Send" subaction on the other instance
  - name: Include Action's Arguments
    type: Checkbox
    required: false
    description: Sends all the action's available arguments to the other instance
  - name: Arguments
    type: List
    required: false
    description: Sends the specified arguments over to the second instance. It's not affected by "Include Action's Arguments" and those arguments are always included.
variables: []
csharpMethods: []
---

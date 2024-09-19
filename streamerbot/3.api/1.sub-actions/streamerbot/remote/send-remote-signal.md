---
title: Send Remote Signal
description: Send a remote signal to another Streamer.bot instance
version: 0.2.4
parameters:
  - name: Instance
    type: Selection
    required: true
    description: Select a specific instance or send it to any
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
variables: []
csharpMethods: []
---

::warning
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::
---
title: Send Remote Trigger
description: Send a trigger to another Streamer.bot instance
version: 0.2.4
parameters:
  - name: Instance
    type: Select
    required: true
    description: |
      Select the instance to send this trigger to

      - `Any` will trigger *all* connected instances

      ::tip{to=/guide/integrations/streamerbot}
      All instances must have the [Streamer.bot Website Integration](/guide/integrations/streamerbot) configured and enabled
      ::
  - name: Event Name
    type: String
    required: true
    description: |
      Name of the event to send.

      - On the receiving instance, enter the same name in the [Remote Instance Trigger](/api/triggers/integrations/streamerbot-remote/remote-instance-trigger) configuration
  - name: Include Action's Arguments
    type: Toggle
    default: 'false'
    description: |
      Send all current action arguments with the trigger to the second instance
  - name: Arguments
    type: List
    description: |
      Define any additional arguments to be sent to the second instance
variables: []
csharpMethods: []
---

::read-more{to=/api/triggers/integrations/streamerbot-remote/remote-instance-trigger}
React to the trigger on your other Streamer.bot instance with the [Remote Instance Trigger](/api/triggers/integrations/streamerbot-remote/remote-instance-trigger)
::
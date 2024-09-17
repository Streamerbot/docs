---
title: Remote Instance Trigger
description: Triggers when a remote Streamer.bot instance trigger gets sent
version: 0.2.4
parameters:
  - name: Instance
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
      Name of the event to trigger on

      - Leave blank to trigger on **any** incoming events
      - To trigger on a specific event, enter the same name configured in the [Send Remote Trigger](/api/triggers/integrations/streamerbot-remote/remote-instance-trigger) sub-action on another instance
variables:
  - name: instanceId
    type: string
    description: The instance ID
    value: dc00c123-456e-789b-ab5e-9a5a8385b85d
  - name: instanceName
    type: string
    description: Name of the instance
    value: Streamer.bot
  - name: instanceVersion
    type: string
    description: Streamer.bot version of the instance
    value: 0.2.4-alpha.18
  - name: instanceOs
    type: string
    description: The operation system of the instance
    value: windows
---

::read-more{to=/api/sub-actions/streamerbot/remote/send-remote-trigger}
This trigger is executed by the [Send Remote Trigger](/api/triggers/integrations/streamerbot-remote/remote-instance-trigger) sub-action, sent from another instance.
::

::tip
Additional variables will be populated for all arguments configured in the sending sub-action
::

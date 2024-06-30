---
title: Remote Instance Trigger
description: Triggers when a remote Streamer.bot instance trigger gets sent
version: 0.2.4
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

::tip
Arguments are getting passed over, so all variables in the action from the sending instance will be available in the receiving instance (if checked)
::

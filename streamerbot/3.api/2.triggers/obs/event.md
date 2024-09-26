---
title: OBS Event
description: Trigger for an OBS Event
version: 0.2.0
parameters:
  - name: ObsConnection
  - name: Event
    type: Select
    required: true
    description: Select an event to Trigger on
variables:
  - name: obs.id
    type: string
    description: The connection id
  - name: obs.name
    type: string
    description: The name of the connection
    value: Main OBS
  - name: obs.host
    type: string
    description: The IP Address of the OBS connection
    value: 127.0.0.1
---

::tip
The variables populated by this trigger are different depending on the `Event` parameter
::

::bookmark{to="https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#events"}
Explore all supported [OBS Studio Events](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#events) on their WebSocket protocol documentation
::
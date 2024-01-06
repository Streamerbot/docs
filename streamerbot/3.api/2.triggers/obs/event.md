---
title: OBS Event
description: Trigger for an OBS Event
version: 0.2.0
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

::callout{icon=i-mdi-bookmark to="https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#events" target=_blank rel=noopener}
Explore all supported [OBS Studio Events](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#events) on their WebSocket protocol documentation
::

## Parameters
::field-group
  ::field{name=OBS type=Select required}
    Choose a configured OBS Connection
    - Select `Any` to trigger on any connection
  ::
  ::field{name=Event type=Select}
    Select an event to react on.
  ::
::

## Variables
The variables of this trigger are different depending on the `Event` parameter.
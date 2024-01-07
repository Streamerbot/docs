---
title: OBS Disconnected
description: Trigger for when OBS is Disconnected
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

## Parameters
::field-group
  ::field{name=OBS type=Select required}
    Choose a configured OBS Connection
    - Select `Any` to trigger on any connection
  ::
::
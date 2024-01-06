---
title: Streamlabs Desktop Disconnected
navigation.title: Disconnected
description: Trigger for when Streamlabs Desktop is Disconnected
version: 0.2.3
variables:
  - name: sd.id
    type: string
    description: The connection id
  - name: sd.name
    type: string
    description: The name of the connection
    value: Main
  - name: sd.host
    type: string
    description: The IP Address of the Streamlabs Desktop connection
    value: 127.0.0.1
---

## Parameters
::field-group
  ::field{name=Instance type=Select required}
    Choose a configured Streamlabs Desktop Connection
    - Select `Any` to trigger on any connection
  ::
::
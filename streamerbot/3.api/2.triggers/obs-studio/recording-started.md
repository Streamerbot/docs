---
title: OBS Recording Started
description: Trigger for when an OBS Recording is Started
version: 0.2.0
parameters:
  - name: Connection
    import: obs-studio/connection
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
  - name: obs.studioVersion
    type: string
    description: The current OBS Studio version
    value: 30.0.0
  - name: obs.websocketVersion
    type: string
    description: The current OBS websocket version
    value: 5.1.0
---
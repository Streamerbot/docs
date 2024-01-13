---
title: Websocket Client Closed
navigation.title: Connection Closed
description: Trigger for when the Websocket Client connection is Closed
version: 0.0.41
variables:
  - name: wsIdx
    type: number
    description: The 0-based id of this websocket
    value: 0, 1, 2, etc.
  - name: wsId
    type: string
    description: The UUID of this websocket client
  - name: wsName
    type: string
    description: The custom defined name of this websocket client
    value: My websocket client
  - name: wsUrl
    type: string
    description: The full URL of this websocket client
    value: ws://127.0.0.1:8080/
  - name: wsScheme
    type: string
    description: The scheme of this websocket client
    value: ws
  - name: wsHost
    type: string
    description: The host of this websocket client
    value: 127.0.0.1
  - name: wsPort
    type: number
    description: The port of this websocket client
    value: 8080
  - name: wsPath
    type: string
    description: The path of this websocket client
    value: /
  - name: wsQuery
    type: string
    description: The query of this websocket client
    value: '?key=value'
---

:image-preview

## Parameters
::field-group
  ::field{name=Client type=Select required}
    Select a client from the Server/Clients -> Websocket Clients tab

    - Select `Any` to trigger on **any client**
  ::
::
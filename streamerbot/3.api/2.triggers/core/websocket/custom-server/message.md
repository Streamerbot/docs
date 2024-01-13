---
title: WebSocket Custom Server Message
navigation.title: Message
description: Trigger for a Websocket Custom Server Connection Message
version: 0.0.41
variables:
  - name: wssIdx
    type: number
    description: The 0-based id of this websocket server
    value: 0, 1, 2, etc.
  - name: wssId
    type: string
    description: The UUID of this websocket server
  - name: ip
    type: string
    description: The ip of this websocket server
    string: 127.0.0.1
  - name: sessionId
    type: string
    description: The session id of the client
  - name: data
    type: string
    description: The received data from the client
---

:image-preview

## Parameters
::field-group
  ::field{name=Server type=Select required}
    Select a server from the Server/Clients -> Websocket Servers tab

    - Select `Any` to trigger on **any server**
  ::
::
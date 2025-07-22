---
title: WebSocket Custom Server Message
navigation.title: Message
description: Trigger for a Websocket Custom Server Connection Message
version: 0.0.41
variables:
  - name: data
    type: string
    description: The received data from the client
    value: Some data
commonVariables:
 - CustomWebsocketServer
---

## Parameters
::field-group
  ::field{name=Server type=Select required}
    Select a server from the Server/Clients -> Websocket Servers tab

    - Select `Any` to trigger on **any server**
  ::
::
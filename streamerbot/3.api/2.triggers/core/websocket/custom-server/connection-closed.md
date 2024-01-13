---
title: WebSocket Custom Server Connection Closed
navigation.title: Connection Closed
description: Trigger for when a Websocket Custom Server Connection is Closed
version: 0.0.41
variables:
  - name: sessionId
    type: string
    description: The session id of the client
---

:image-preview

## Parameters
::field-group
  ::field{name=Server type=Select required}
    Select a server from the Server/Clients -> Websocket Servers tab

    - Select `Any` to trigger on **any server**
  ::
::
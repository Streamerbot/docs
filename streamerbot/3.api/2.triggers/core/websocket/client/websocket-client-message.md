---
title: Websocket Client Message
navigation.title: Message
description: Trigger for a the Websocket Client Message
version: 0.0.41
variables:
  - name: message
    type: string
    description: The websocket client message
    value: '{"timeStamp":"2023-03-16T22:58:28.3298+01:00","event":{"source":"HotKey","type":"Press"},"data":{"_85lbxopeOGvkNXq7iRgrjS6tpjj":1,"_hdhxue62iGbvG5rnMWU0dxGe29p":96}}'
commonVariables:
  - WebsocketClient
---

## Parameters
::field-group
  ::field{name=Client type=Select required}
    Select a client from the Server/Clients -> Websocket Clients tab

    - Select `Any` to trigger on **any client**
  ::
::
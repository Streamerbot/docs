---
description: Broadcast a message to a custom WebSocket server
parameters:
  - name: data
    description: |
      Data to be sent to connected clients

      JSON must be stringified.
    value: '"Hello, world!"'
  - name: sessionId
    description: The client session you want to send the message to. `null` will send to all connected clients.
    value: 'null'
  - name: connection
    description: |
      The Custom Websocket Server connection to send the message to

      Zero-indexed based on the order you see in `Servers/Clients > Websocket Servers`<br>
      e.g. The first server in the list is `0`, the second server in the list is `1`, and so on...
    value: 0
---
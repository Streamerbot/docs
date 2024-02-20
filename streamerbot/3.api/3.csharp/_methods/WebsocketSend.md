---
description: Send data over a configured WebSocket client
parameters:
  - name: data
    description: The data to send
    value: '"Hello, world!"'
  - name: connection
    description: |
      The configured WebSocket client connection send the message with

      Zero-indexed based on the order you see in `Servers/Clients > Websocket Clients`<br>
      e.g. The first client in the list is `0`, the second client in the list is `1`, and so on...
    value: 0
---
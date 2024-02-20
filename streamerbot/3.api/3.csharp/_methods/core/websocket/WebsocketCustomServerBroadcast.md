---
description: Broadcast a message to a custom WebSocket server
parameters:
  - name: data
    description: |
      Data to be sent to connected clients

      JSON must be stringified.
    value: '"Hello, world!"'
  - import: WebsocketCustomServerConnection
---
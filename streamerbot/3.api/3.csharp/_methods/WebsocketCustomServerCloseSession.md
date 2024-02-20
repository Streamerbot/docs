---
description: Disconnect a session from a custom WebSocket server
parameters:
  - name: sessionId
    description: The unique id of the client session to disconnect
    value: '"JdHd4aVd"'
  - name: connection
    description: |
      The index of the Websocket Server

      Zero-indexed based on the order you see in `Servers/Clients > Websocket Servers`<br>
      e.g. The first server in the list is `0`, the second server in the list is `1`, and so on...
    value: 0
---
---
navigation.title: Message
---

# WebSocket Custom Server Message
Triggered when a client sends a message to a custom WebSocket server

## Parameters

### `Server`
Select any or a specific websocket server

## Variables
:variables-description

Name | Description
----:|:------------
`wssIdx` | The 0-based id of this websocket server e.g. `0`, `1`, `2`, etc.
`wssId` | The UUID of this websocket server.
`ip` | The ip of this websocket server e.g. `127.0.0.1`
`sessionId` | The session id of the client.
`data` | The received data from the client.
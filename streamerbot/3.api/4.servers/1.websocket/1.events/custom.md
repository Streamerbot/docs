---
title: Custom
description: Emit custom events from the Streamer.bot WebSocket server
---

## Overview
You can enable `Custom` events with this [Subscribe](/api/servers/websocket/requests#subscribe) request:

```json [Subscribe Request]
{
  "request": "Subscribe",
  "id": "my-request-id",
  "events": {
    "General": [
      "Custom"
    ]
  },
}
```

## C# Methods
### `WebsocketBroadcastString`
Send a custom string over the Streamer.bot WebSocket server
:csharp-method{name=WebsocketBroadcastString}
::code-group
  ```cs [Example Request]
  CPH.WebsocketBroadcastString("Hello, world!");
  ```
  ```json [Example Response]
  {
    "timeStamp": "2023-01-01-05T00:25:18.2696998+01:00",
    "event": {
      "source": "General",
      "type": "Custom",
      "data": "Hello, world!"
    }
  }
  ```
::

### `WebsocketBroadcastJson`
Send a custom JSON event over the Streamer.bot WebSocket server
:csharp-method{name=WebsocketBroadcastJson}
::code-group
  ```ts [Example Request]
  CPH.WebsocketBroadcastJson("{'key': 'value'}");
  ```
  ```json [Example Response]
  {
    "timeStamp": "2023-01-01-05T00:25:18.2696998+01:00",
    "event": {
      "source": "General",
      "type": "Custom",
      "data": {
        "key": "value"
      }
    }
  }
  ```
::
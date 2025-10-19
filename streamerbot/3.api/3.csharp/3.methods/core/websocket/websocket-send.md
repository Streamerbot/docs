---
name: WebsocketSend
title: WebsocketSend
description: Send data over a configured WebSocket client
parameters:
  - name: data
    description: The data to send
    default: '"Hello, world!"'
  - name: connection
    import: core/websocket/custom-clients/connection
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Send "Hello, world!" over the custom Websocket Client with index 0
            //Index is from top to bottom of the clients list, starting at 0
            CPH.WebsocketSend("Hello, world!", 0);

            return true;
        }
    }
---
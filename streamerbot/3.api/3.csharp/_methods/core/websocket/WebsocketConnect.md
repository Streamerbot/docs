---
description: Connect a configured WebSocket client
parameters:
  - import: WebsocketClientConnection
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Connect the websocket client with index 0
            //Index is from top to bottom of the clients list, starting at 0
            CPH.WebsocketConnect(0);
            
            return true;
        }
    }
---
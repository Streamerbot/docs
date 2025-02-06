---
description: Stop a custom WebSocket server
parameters:
  - import: WebsocketCustomServerConnection
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Stop the custom websocket server with index 0
            //Index is from top to bottom of the clients list, starting at 0
            CPH.WebsocketCustomServerStop(0);
            
            return true;
        }
    }
---
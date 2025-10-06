---
name: WebsocketCustomServerStart
title: WebsocketCustomServerStart
description: Start a custom WebSocket server
parameters:
  - import: WebsocketCustomServerConnection
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Start the custom websocket server with index 0
            //Index is from top to bottom of the clients list, starting at 0
            CPH.WebsocketCustomServerStart(0);
            
            return true;
        }
    }
---
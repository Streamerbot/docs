---
name: WebsocketDisconnect
title: WebsocketDisconnect
description: Disconnect a configured WebSocket client
parameters:
  - name: connection
    import: core/websocket/custom-clients/connection
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Disconnect the websocket client with index 0
            //Index is from top to bottom of the clients list, starting at 0
            CPH.WebsocketDisconnect(0);

            return true;
        }
    }
---
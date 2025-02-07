---
description: Broadcast a message to a custom WebSocket server
parameters:
  - name: data
    description: |
      Data to be sent to connected clients

      JSON must be stringified.
    default: '"Hello, world!"'
  - import: WebsocketCustomServerConnection
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define data
            string data = "Kachow";
            //Define session Id
            string sessionId = "JdHd4aVd";
            
            //Send data "Kachow" to specific session via specific websocket server
            //Index is from top to bottom of the clients list, starting at 0
            CPH.WebsocketCustomServerBroadcast(data, sessionId, 0);
            
            return true;
        }
    }
---
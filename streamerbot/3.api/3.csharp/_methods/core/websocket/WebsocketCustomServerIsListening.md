---
description: Check if a custom WebSocket server is currently listening for connections
parameters:
  - import: WebsocketCustomServerConnection
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Check the custom websocket server with index 0 is listening
            //Index is from top to bottom of the clients list, starting at 0
            bool isListening = CPH.WebsocketCustomServerIsListening(connection);
            
            if(isListening){
              CPH.SendMessage("Websocket server is listening!");
            }

            return true;
        }
    }
---
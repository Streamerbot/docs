---
description: Get the connection index of a custom WebSocket server
parameters:
  - name: name
    description: The configured name of the WebSocket server
    default: '"My WebSocket Server"'
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get index of custom websocket server named "Test"
            //Index is from top to bottom of the clients list, starting at 0
            int index = CPH.WebsocketCustomServerGetConnectionByName("Test");
            
            return true;
        }
    }
---
---
description: Send a JSON payload to all clients connected to the Streamer.bot [WebSocket Server](/api/servers/websocket/requests)
parameters:
  - name: data
    description: The stringified JSON payload to send to clients
    default: '"{\"foo\":\"bar\"}"'
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define data you want to send
            string json = "{\"foo\":\"bar\"}";

            //Broadcast data to clients
            CPH.WebsocketBroadcastJson(data);
            
            return true;
        }
    }
---
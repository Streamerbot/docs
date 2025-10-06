---
name: WebsocketBroadcastString
title: WebsocketBroadcastString
description: Send a text string to all clients connected to the Streamer.bot [WebSocket Server](/api/websocket/requests)
parameters:
  - name: data
    description: The text to send to connected clients
    default: '"Hello, world!"'
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define data you want to send
            string data = "Hello, world!";

            //Broadcast data to clients
            CPH.WebsocketBroadcastString(data);

            return true;
        }
    }
---
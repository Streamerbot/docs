---
name: WebsocketIsConnected
title: WebsocketIsConnected
description: Check if a configured WebSocket client is connected
parameters:
  - import: WebsocketClientConnection
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Check if the custom websocket client with index 0 is connected
            //Index is from top to bottom of the clients list, starting at 0
            bool isConnected = CPH.WebsocketIsConnected(0);
            
            if(isConnected){
              CPH.SendMessage("Websocket client is connected!");
            }

            return true;
        }
    }
---
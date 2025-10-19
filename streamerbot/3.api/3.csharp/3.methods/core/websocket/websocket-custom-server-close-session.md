---
name: WebsocketCustomServerCloseSession
title: WebsocketCustomServerCloseSession
description: Disconnect a session from a custom WebSocket server
parameters:
  - name: sessionId
    description: The unique id of the client session to disconnect
    default: '"JdHd4aVd"'
  - name: connection
    import: core/websocket/custom-servers/connection
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define session Id
            string sessionId = "JdHd4aVd";

            //Close session of custom websocket server index 0
            //Index is from top to bottom of the clients list, starting at 0
            CPH.WebsocketCustomServerCloseSession(sessionId, 0);

            return true;
        }
    }
---
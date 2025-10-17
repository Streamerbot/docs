---
name: WebsocketCustomServerCloseAllSessions
title: WebsocketCustomServerCloseAllSessions
description: Disconnect all client sessions from a custom WebSocket server
parameters:
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

            //Close all sessions of custom websocket server index 0
            //Index is from top to bottom of the clients list, starting at 0
            CPH.WebsocketCustomServerCloseAllSessions(0);

            return true;
        }
    }
---
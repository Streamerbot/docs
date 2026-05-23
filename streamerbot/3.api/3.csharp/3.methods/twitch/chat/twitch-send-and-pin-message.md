---
name: TwitchSendAndPinMessage
title: TwitchSendAndPinMessage
description: Send a chat message and automatically pin it for 20 minutes
version: 1.0.5
parameters:
    - name: message
      description: The message to send to chat and pin
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            // set message for chat
            string message = "This is a pinned chat message";        

            // Send the message to chat, and automatically pin it
            CPH.TwitchSendAndPinMessage(message);

            return true;
        }
    }
---

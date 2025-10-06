---
name: TwitchClearChatMessages
title: TwitchClearChatMessages
description: Clear Twitch Chat
parameters:
  - name: bot
    default: true
    description: |
      - `true`{lang=cs} - Clear all messages with bot account
      - `false`{lang=cs} - Clear all messages with broadcaster account
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Clear chat
            bool gotCleared = CPH.TwitchClearChatMessages(true);
            
            if(gotCleared){
                CPH.SendMessage("Message got cleared successfully!");
            }
            return true;
        }
    }
---

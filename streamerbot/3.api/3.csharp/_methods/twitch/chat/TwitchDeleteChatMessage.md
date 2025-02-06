---
description: Delete Twitch message via message id
parameters:
  - name: messageId
    default: '"abcde12345"'
    description: Id of the message you want to delete
  - name: bot
    default: true
    description: |
      - `true`{lang=cs} - Delete the message with bot account
      - `false`{lang=cs} - Delete the message with broadcaster account
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Set message for chat
            CPH.TryGetArg("msgId",out string messageId);

            //Delete the message that was just send by a command/message
            bool gotDeleted = CPH.TwitchDeleteChatMessage(messageId, true);
            
            if(gotDeleted){
                CPH.SendMessage("Message got deleted successfully!");
            }
            return true;
        }
    }
---

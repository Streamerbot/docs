---
description: Send a reply to a specific Twitch chat message
parameters:
  - name: message
    value: '"Hello, world!"'
    description: Enter the message contents
  - name: replyId
    value: 'args["msgId"]'
    description: Enter the unique ID of the message to reply to
  - name: bot
    value: true
    description: |
      - `true`{lang=cs} - Send the reply using your **Twitch Bot** account
      - `false`{lang=cs} - Send the reply using your **Twitch Broadcaster** account
  - name: fallback
    version: 0.2.5
    value: true
    description: |
      -`true`{lang=cs} - (If `bot` bool is set to `True`), this is the same behaviour as if you had Bot as your preferred account.
      -`false`{lang=cs} - (If `bot` bool is set to `True`), it will try to send using **only** the Bot account, and do **nothing** if it can't (i.e, not logged in).
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get message id to reply to
            CPH.TryGetArg("msgId",out string messageId);

            //Set message for reply
            string message = "This is a test reply.";

            //Send reply with bot account
            CPH.TwitchReplyToMessage(message, messageId, true, true);

            return true;
        }
    }
---

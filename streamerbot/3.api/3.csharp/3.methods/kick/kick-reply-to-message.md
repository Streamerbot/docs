---
name: KickReplyToMessage
title: KickReplyToMessage
description: Send a reply to a specific Kick chat message
version: 1.0.0
parameters:
  - name: message
    default: '"Hello, world!"'
    description: Enter the message contents
  - name: replyId
    default: 'args["messageId"]'
    description: Enter the unique ID of the message to reply to
  - name: useBot
    default: true
    description: |
      - `true`{lang=cs} - Send the reply using your **Kick Bot** account
      - `false`{lang=cs} - Send the reply using your **Kick Broadcaster** account
  - name: fallback
    default: true
    description: |
      - `true`{lang=cs} - (If `bot` bool is set to `True`), this is the same behavior as if you had Bot as your preferred account.
      - `false`{lang=cs} - (If `bot` bool is set to `True`), it will try to send using **only** the Bot account, and do **nothing** if it can't (i.e, not logged in).
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get message id to reply to
            CPH.TryGetArg("messageId", out string messageId);

            //Set message for reply
            string message = "This is a test reply.";

            //Send reply with bot account
            CPH.KickReplyToMessage(message, messageId, true, true);

            return true;
        }
    }
---
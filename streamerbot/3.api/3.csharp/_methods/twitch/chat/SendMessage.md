---
description: Sends a Twitch chat message using either Twitch Broadcaster or Twitch Bot account
parameters:
  - name: message
    value: '"Hello, world!"'
    description: Enter the message contents
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
            //Set message for chat
            string message = "This is a test message.";

            //Send reply with bot account
            CPH.SendMessage(message, true, true);

            return true;
        }
    }
---

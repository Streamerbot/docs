---
description: Sends an Action from either the Twitch Broadcaster or Twitch Bot Account (denoted by *Italics* in Twitch chat)
version: 0.2.5
parameters:
  - name: action
    value: '"Action Name"'
    description: Enter the name of the Action exactly as it appears in Streamer.bot
  - name: bot
    value: true
    description: |
      - `true`{lang=cs} - Send the Action using your **Twitch Bot** account
      - `false`{lang=cs} - Send the Action using your **Twitch Broadcaster** account
  - name: fallback
    value: true
    description: |
      - `true`{lang=cs} - (If `bot` bool is set to `True`), this is the same behaviour as if you had Bot as your preferred account.
      - `false`{lang=cs} - (If `bot` bool is set to `True`), it will try to send using **only** the Bot account, and do **nothing** if it can't (i.e, not logged in).
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {

            //Set Action name here
            string action = "Test Action Name";

            //Send reply with bot account
            CPH.SendAction(action, true, true);

            return true;
        }
    }
---

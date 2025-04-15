---
description: Sends a Twitch chat message using either Twitch Broadcaster or Twitch Bot account
parameters:
  - name: message
    default: '"Hello, world!"'
    description: Enter the message contents
  - name: useBot
    default: true
    description: |
      - `true`{lang=cs} - Send the message using your **Twitch Bot** account
      - `false`{lang=cs} - Send the message using your **Twitch Broadcaster** account
   - name: color
    default: "Default"
    description: |
      Select the color for the announcement. Valid values are:  
      - `Default` – Standard color  
      - `Blue`  
      - `Green`  
      - `Orange`  
      - `Purple`
  - name: fallback
    version: 0.2.5
    default: true
    description: |
      - `true`{lang=cs} - (If `bot` bool is set to `True`), this is the same behaviour as if you had Bot as your preferred account.
      - `false`{lang=cs} - (If `bot` bool is set to `True`), it will try to send using **only** the Bot account, and do **nothing** if it can't (i.e, not logged in).
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Set message for chat
            string message = "This is an announcement";

            //Send announcement with bot account, or fallback to broadcaster
            CPH.TwitchAnnounce(message, true, color, true);

            return true;
        }
    }
---

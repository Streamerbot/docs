---
description: |
  Send a Twitch Whipser to another user.

  There are Twich limitations you have to consider before using this method:
  - The user sending the whisper must have a verified phone number.
  - The API may silently drop whispers that it suspects of violating Twitch policies.
  - Rate Limits: You may whisper to a maximum of 40 unique recipients per day. Within the per day limit, you may whisper a maximum of 3 whispers per second and a maximum of 100 whispers per minute.
parameters:
  - name: userName
    default: '"streamerdotbot"'
    description: Login name of the user you want to send a whisper to
  - name: message
    default: '"Hello, world!"'
    description: Enter the message contents
  - name: bot
    default: true
    description: |
      - `true`{lang=cs} - Send the message using your **Twitch Bot** account
      - `false`{lang=cs} - Send the message using your **Twitch Broadcaster** account
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define user login you want to whisper
            string userName = "streamerdotbot";
            //Set message for chat
            string message = "This is a test message.";

            //Send message with bot account
            bool wasSend = CPH.SendWhisper(userName, message, true);
            
            if(wasSend){
                //This does not mean that is was received by the user.
                //It may still be silently dropped by Twitch
                CPH.LogInfo("Whisper was send!");
            }
            return true;
        }
    }
---

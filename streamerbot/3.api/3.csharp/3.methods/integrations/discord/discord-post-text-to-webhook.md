---
name: DiscordPostTextToWebhook
title: DiscordPostTextToWebhook
description: Send simple text content to Discord webhook
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define your webhook url
            string webhookUrl = "Write your webhook url in here";
            //Set whether it should be textToSpeech in Discord when send
            bool textToSpeech = false;

            //Get user name of current user
            CPH.TryGetArg("user",out string user);
            //Get for example command input and set as content variable
            CPH.TryGetArg("rawInput",out string content);
            
            //Send Webhook message example, if needed you can save the messageId that gets returned (0.2.4+ only)
            string messageId = CPH.DiscordPostTextToWebhook(webhookUrl, content, $"{user} said:", "", textToSpeech);
            
            return true;
        }
    }
---

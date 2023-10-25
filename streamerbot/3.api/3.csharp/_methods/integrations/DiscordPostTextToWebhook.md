::code-group
  ```csharp [Method]
  bool DiscordPostTextToWebhook(string webhookUrl, string content, string username = null, bool textToSpeech = false);
  ```
  ```csharp [Example]
  CPH.DiscordPostTextToWebhook("https://discord.com/api/webhooks/1117864124892494336/COYRgS3kkhWqL3TovardWWrAGOUi7UeRApVxQl-Oxyo1JiAR5vGuiIZ511DPwxZlPsJO", "Hello, Discord!");
  ```
::
---
title: Basic Webhook
description: Post messages to a Discord channel with webhooks
version: 0.1.14
parameters:
  - name: Webhook Name
    required: true
    type: Text
    description: |
      Enter a name for your Webhook

      _Variables are not supported_
  - name: Username
    type: Text
    default: Username configured in Discord Webhook settings
    description: Set a custom username for the author of the resulting Discord message
  - name: Webhook URL
    required: true
    type: Text
    description: |
      Enter the Webhook URL copied from the [Discord webhook configuration](/guide/integrations/discord)

      _Variables are not supported_
  - name: Content
    required: true
    type: Text
    description: |
      Enter the text content for your webhook message. Multiple lines and variables are supported.

      ::collapsible{name="details for pinging users or roles"}
      1. Enable Developer Mode

          Enable developer mode in Discord by opening settings and navigating to `App Settings -> Advanced`. Then, enable the `Developer Mode` toggle.

      2. User Pings

          Users can be pinged in the following format:

          `<@DISCORD_USER_ID>` e.g. `<@0123456789>`

          With developer mode enabled, you can right-click on any user in discord, and click `Copy ID` to obtain their user ID.

      3. Role Pings

          Roles can be pinged in the following format:

          `<@&DISCORD_ROLE_ID>` e.g. `<@&0123456789>`

          With developer mode enabled, you can right-click on a role in the server settings area, and click `Copy ID` to obtain its ID.
      ::
  - name: Avatar URL
    type: Text
    default: Avatar configured in Discord Webhook settings
    description: |
      Set a custom avatar for the author of the resulting Discord message

      For example, you could set it to a chat user's profile picture by using the [Get User Info for Target](/Sub-Actions/Twitch/Get-User-Info-for-Target) Sub-Action and then using the `%targetUserProfileImageUrl%` variable.
  - name: Text to Speech
    type: Toggle
    default: false
    description: Toggle to send the message with Discord TTS

csharpMethods:
  - DiscordPostTextToWebhook
---

::read-more{to=/guide/integrations/discord}
If you have not already configured a Webhook for your Discord server, check out the
[Discord configuration guide](/guide/integrations/discord) to learn how.
::
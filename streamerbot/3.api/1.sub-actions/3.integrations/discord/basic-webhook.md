---
version: 0.1.14
---

# Basic Webhook
Post messages to a [Discord](https://discord.gg) channel via Webhooks
:image-preview{width=400}

::list
- If you have not already configured a Webhook for your Discord server, check out the
[Discord configuration guide](/guide/integrations/discord) to learn how.
::

Username, content, and image can contain variables and will be parsed.
Username, and image are also optional

## Parameters
### `Webhook Name`
Enter a name for your webhook
::list{type=warning}
- Variables are **not** supported
::

### `Username`
Set a custom username for the author of the resulting Discord message
::list
- *Optional*
- By default Discord will use the name configured in the webhook settings
::

### `Webhook URL`
Enter the Webhook URL copied from the [Discord webhook configuration](/guide/integrations/discord)
::list{type=warning}
- Variables are **not** supported
::

### `Content`
Enter the text content for your Webhook message
::list
- You can use <kbd>Ctrl+Enter</kbd> for multiple lines
::

::disclosure{icon=mdi:discord style="margin-top: 1rem;"}
If you would like to ping users or roles, click here to learn more!

#content
#### Enable Developer Mode
Enable developer mode in Discord by opening settings and navigating to `App Settings -> Advanced`. Then, enable the `Developer Mode` toggle.

#### User Pings
Users can be pinged in the following format:

`<@DISCORD_USER_ID>` e.g. `<@0123456789>`

With developer mode enabled, you can right click on any user in discord, and click `Copy ID` to obtain their user ID.

#### Role Pings
Roles can be pinged in the following format:

`<@&DISCORD_ROLE_ID>` e.g. `<@&0123456789>`

With developer mode enabled, you can right click on a role in the server settings area, and click `Copy ID` to obtain its ID.
::


### `Avatar URL`
Set a custom avatar for the author of the resulting Discord message
::list
- *Optional*
- By default Discord will use the avatar configured in the webhook settings
::
Here you can optionally fill out an URL to temporarily change the avatar of the webhook to something to your choose, an example use case for this is adding a Chat Message event and using the user's profile image in this field with the [Get User Info for Target](/Sub-Actions/Twitch/Get-User-Info-for-Target) Sub-Action and then using the `%targetUserProfileImageUrl%` variable.

### `Image`
Add an image embed to the Webhook message
::list
- *Optional*
::

### `Text to Speech`
Toggle to send the message with Discord TTS

## C# Usage
:csharp-method{name=DiscordPostTextToWebhook}
---
title: Discord
description: Integrate Streamer.bot with Discord via webhooks
navigation.icon: null
icon: i-mdi-discord
version: 0.1.14
logo: https://streamer.bot/img/integrations/discord.png
---

Webhooks allow you to send messages to your [Discord](https://discord.gg) servers with ease.

::warning
You must have the proper permissions to create webhooks on a given server/channel
::

## Configuration

1. Create a Discord Webhook

    ::navigate
    On Discord, navigate to **Edit Channel > Integrations**
    ::

    - Click `Create Webhook`

    ![Discord Webhook Configuration](assets/discord-webhook.png)

    - Configure the `Name` and `Avatar` as you wish
    - Click the `Copy Webhook URL` button to get your Webhook URL

2. Done!

    ::success
    You can now use the copied Webhook URL with the [Discord Webhook](/api/sub-actions/integrations/discord/basic-webhook) sub-action!
    ::

## Usage
:api-reference-cards{path=integrations/discord}
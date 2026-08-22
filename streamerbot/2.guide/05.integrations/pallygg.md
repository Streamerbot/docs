---
title: Pally.gg
description: Integrate Streamer.bot with Pally.gg
navigation.icon: null
version: 0.2.4
logo: /img/icons/pallygg.svg
---

Integrate Streamer.bot with [Pally.gg](https://pally.gg){target=\_blank}

## Configuration

::steps{level=3}

### Obtain a Pally.gg API Key

:::navigate{to="https://pally.gg" target=\_blank rel=noreferer}
Navigate to the [Pally.gg](https://pally.gg){target=\_blank rel=noreferer} website
:::

1. Sign in to your account
1. From the dashboard, click the upper right drop down and goto `Settings`
1. On the left side under `Account Settings`, click `API Keys`
1. Click `Create new API key`
1. Click the Copy icon to copy the key and proceed below

### Configure Streamer.bot

:::navigate
In Streamer.bot, navigate to **Integrations > Pally.gg**
:::

1. Paste the copied API key in the API Key field
1. Enable `Auto Connect` to automatically connect to Pally.gg when Streamer.bot starts up
1. Enable `Auto Reconnect` to automatically reconnect to Pally.gg if the connection is disrupted

:::success
Pally.gg is now connected!
:::

::

## Options

::field-group
:::field{name="API Key" type="Text" required}
The API Key from your Pally.gg account
:::

:::field{name="Auto Connect on Startup" type=Toggle}
Automatically connect to Pally.gg when Streamer.bot starts up
:::

:::field{name="Auto Reconnect" type=Toggle}
Automatically reconnect to Pally.gg when the connection is disrupted
:::
::

## Usage

:read-more{to="/api/triggers/integrations/pallygg"}

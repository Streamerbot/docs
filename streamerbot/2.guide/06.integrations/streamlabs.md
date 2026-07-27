---
title: Streamlabs
description: Integrate Streamer.bot with your Streamlabs account
icon: simple-icons:streamlabs
navigation.icon: null
logo: /img/icons/streamlabs.png
---

The [Streamlabs](https://streamlabs.com){target=\_blank} integration allows you to receive donation and merchandise events in Streamer.bot

::read-more{to=/guide/stream-apps/streamlabs-desktop}
If you are looking for the [Streamlabs Desktop](/guide/stream-apps/streamlabs-desktop) stream app integration, click here to read more.
::

## Configuration

::steps{level=3}

### Obtain your Streamlabs API Token

:::navigate{to="https://streamlabs.com/dashboard#/settings/api-settings" target=\_blank rel=noopener}
On the [Streamlabs](https://streamlabs.com/dashboard#/settings/api-settings) website, navigate to **Dashboard > Settings > API Settings > API Tokens**
:::

1. Next to `Your Socket API Token`, click `Copy` to obtain your API token

### Configure Streamer.bot

:::navigate
In Streamer.bot, navigate to **Integrations > Streamlabs**
:::

1. Paste your `Socket API Token` into the `Token` field
2. Click `Connect to Streamlabs`
3. Enable `Auto Connect` to automatically connect to Streamlabs when Streamer.bot starts up
4. Enable `Auto Reconnect` to automatically reconnect to Streamlabs if the connection is disrupted

:::success
Streamlabs is now connected with Streamer.bot!
:::

::

## Usage

:read-more{to="/api/triggers/integrations/streamlabs"}

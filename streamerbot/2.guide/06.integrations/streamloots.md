---
title: StreamLoots
description: Integrate Streamer.bot with StreamLoots
navigation.icon: null
version: 1.0.5
logo: /img/icons/streamloots.png
---

Integrate Streamer.bot with [StreamLoots](https://streamloots.com){target=\_blank}

## Configuration

::steps{level=3}

### Sign in to the StreamLoots Website

1. Follow the instructions on the StreamLoots website and login with your preferred OAuth provider

### Navigate to the StreamLoots Alerts Page

1. Open the StreamLoots website
1. Find the page with your Alerts Widget URL (e.g. `https://streamloots.com/your_username/widgets/alerts`)
1. Press the `"Copy"` button to copy your Alerts Widget URL - _you will need this for the next step when configuring StreamLoots!_


### Setup the Connection in Streamer.bot

:::navigate
In Streamer.bot, navigate to **Integrations > StreamLoots**
:::

1. Enable `Auto Connect` to automatically connect to StreamLoots when Streamer.bot starts up
1. Enable `Auto Reconnect` to automatically reconnect to StreamLoots if the connection is disrupted
1. Paste your Alerts Widget URL into the `Alerts Widget URL` input
1. Click `Connect` to start the Connection for the first time (You will notice the word `'Connected'` under the `Connection Status` if the connection is successful)

:::success
StreamLoots is now connected to Streamer.bot!
:::

## Usage

:read-more{to="/api/triggers/integrations/streamloots"}
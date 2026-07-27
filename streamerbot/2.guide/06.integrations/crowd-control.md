---
title: Crowd Control
description: Integrate Streamer.bot with Crowd Control
navigation.icon: null
version: 0.2.0
logo: /img/icons/crowd-control.svg
---

Integrate Streamer.bot with [Crowd Control](https://crowdcontrol.live){target=\_blank}

## Configuration

::steps{level=3}

### Get Overlay URL

First, we need to obtain your personal `Overlay URL` from the Crowd Control application, which will allow Streamer.bot to receive events from Crowd Control.

::navigate
Navigate to **Overlay > Assets** in the Crowd Control application
::

- Click the :kbd{value=Copy} button next to your `Overlay URL`

### Configure Streamer.bot

::navigate
Navigate to **Integrations > Crowd Control** in Streamer.bot
::

- Paste the copied URL into the `Overlay URL` text field

::success
Crowd Control is now connected to Streamer.bot!
::
::

## Options

::field-group
:::field{name="Overlay URL" type="Text" required}
Your personal Overlay URL from the Crowd Control application
:::

:::field{name="Auto Connect on Startup" type=Toggle}
Automatically connect to Crowd Control when Streamer.bot starts up
:::

:::field{name="Auto Reconnect" type=Toggle}
Automatically reconnect to Crowd Control when the connection is disrupted
:::
::

## Usage

:read-more{to="/api/triggers/integrations/crowdcontrol"}

---
title: Crowd Control
description: Integrate Streamer.bot with Crowd Control
navigation.icon: null
version: 0.2.0
logo: /img/icons/crowd-control.svg
---

Integrate Streamer.bot with [Crowd Control](https://crowdcontrol.live){target=_blank}

## Configuration

1. Obtain your Crowd Control Overlay URL

    ::navigate
    Navigate to **Overlay > Assets** in the Crowd Control application
    ::

    - Click the :shortcut{value=Copy} button next to your `Overlay URL`

    ![image](https://github.com/Streamerbot/docs/assets/8848167/d7b2db23-313a-40fa-b883-180d204ee7ce)

2. Configure Streamer.bot

    ::navigate
    Navigate to **Integrations > Crowd Control** in Streamer.bot
    ::

    - Paste the copied URL into the `Overlay URL` text field

3. Done!

    ::success
    Crowd Control is now connected to Streamer.bot!
    ::

## Options
::field-group
  ::field{name="Overlay URL" type="Text" required}
  Your personal Overlay URL from the Crowd Control application
  ::
   ::field{name="Auto Connect on Startup" type=Toggle}
  Automatically connect to Crowd Control when Streamer.bot starts up
  ::

  ::field{name="Auto Reconnect" type=Toggle}
  Automatically reconnect to Crowd Control when the connection is disrupted
  ::
::

## Usage
:api-reference-cards{path=integrations/crowdcontrol}
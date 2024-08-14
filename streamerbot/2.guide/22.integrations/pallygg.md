---
title: Pally.gg
description: Integrate Streamer.bot with Pally.gg
navigation.icon: null
version: 0.2.4
badge: New
logo: /img/icons/pallygg.svg
---

Integrate Streamer.bot with [Pally.gg](https://pally.gg){target=_blank}

## Configuration

1. Obtain a Pally.gg API Key

    ::navigate{to="https://pally.gg" target=_blank rel=noreferer}
    Navigate to the Pally.gg website
    ::

    1. Sign in to your account
    2. From the dashboard, click the upper right drop down and goto `Settings`
    3. On the left side under `Account Settings`, click `API Keys`
    4. Click `Create new API key`
    5. Click the Copy icon to copy the key and proceed below

2. Connect Streamer.bot

    ::navigate
    In Streamer.bot, navigate to **Integrations > Pally.gg**
    ::

    1. Paste the copied API key in the API Key field
    2. Enable `Auto Connect` to automatically connect to Pally.gg when Streamer.bot starts up
    3. Enable `Auto Reconnect` to automatically reconnect to Pally.gg if the connection is disrupted

3. Done!

    ::success
    Pally.gg is now connected!
    ::

## Options
::field-group
  ::field{name="API Key" type="Text" required}
  The API Key from your Pally.gg account
  ::
   ::field{name="Auto Connect on Startup" type=Toggle}
  Automatically connect to Pally.gg when Streamer.bot starts up
  ::

  ::field{name="Auto Reconnect" type=Toggle}
  Automatically reconnect to Pally.gg when the connection is disrupted
  ::
::

## Usage
:api-reference-cards{path=integrations/pallygg}
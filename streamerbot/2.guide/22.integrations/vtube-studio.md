---
title: VTube Studio
description: Integrate Streamer.bot with VTube Studio
icon: IconVtubeStudio
navigation.icon: null
version: 0.2.0
logo: /img/icons/vtube-studio.png
---

## Configuration

1. Enable the VTube Studio API
    ::navigate
    Navigate to **Settings** in VTube Studio
    ::

    - Enable the `Start API` toggle
      ![VTube Studio Start API](assets/vtube-studio-enable-api.png){width=400}

2. Configure Streamer.bot
    ::navigate
    Navigate to **Integrations > VTube Studio** in Streamer.bot
    ::

    - Match the settings to those configured in VTube Studio
        - `Host` defaults to `localhost`
        - `Port` defaults to `8001`
    - Check `Auto Connect` and `Auto Reconnect` if you want (optional).
    - Hit `Connect`

    ![VTube Studio SB Menu](assets/vtube-studio-connect.png)

3. Allow the connection

    Quickly return VTube Studio and allow the connection.
    ![VTube Studio SB Menu](assets/vtube-studio-allow-connection.png){width=400}

4. Done!
   ::success
   Streamer.bot and VTube Studio are now connected!
   ::

## Usage

:api-reference-cards{path=integrations/vtube-studio}

---
title: AutoHotKey Actions
description: Execute your Streamer.bot actions with AutoHotKey
author: Whipstickgostop
icon: i-simple-icons-autohotkey
navigation: false
difficulty: 2
---

You can use [AutoHotKey](https://www.autohotkey.com){target=_blank rel=noopener} to execute your Streamer.bot Actions in realtime via the [UDP Server](/api/servers/udp)

:read-more{to="/api/servers/udp"}

## Prerequisites

1. Install AutoHotKey v2

    Navigate to the [AutoHotKey](https://www.autohotkey.com){target=_blank rel=noopener} website to download and install AutoHotKey v2

2. Download Example Scripts

    `Whipstickgostop/streamerbot-ahk` is available on [GitHub](https://github.com/Whipstickgostop/streamerbot-ahk) or [direct download](https://github.com/Whipstickgostop/streamerbot-ahk/archive/refs/heads/main.zip)

## Instructions

1. Enable the Streamer.bot UDP Server

    ::navigate
    Navigate to **Servers/Clients > UDP Server** in Streamer.bot
    ::

    - Enable `Auto Start` and then start the UDP Server

2. Open Example Script in Editor

    - Extract the `streamerbot-ahk` zip to any location.
    - Open the extracted folder and then open the `example-do-action.ahk` in any text editor.

3. Update Connection Settings

    - If you changed UDP Server settings in Streamer.bot, update the `StreamerbotUDP` connection details to match your configuration.

4. Configure HotKeys
    - By default, the script is configured with hotkeys on <kbd>F12</kbd> and <kbd>F11</kbd>.
    - You can add or modify any hotkeys as needed.

    ::read-more{to=https://www.autohotkey.com/docs/v2/Hotkeys.htm}
    Refer to the **AutoHotKey** documentation for setting various hotkeys
    ::

5. Update Action IDs

    1. In Streamer.bot, <kbd>Right-Click</kbd> on the action you want to execute from AHK, and select `Copy Action ID`
    2. Update the `sb.DoAction("<action-id>")`{lang=cs} lines to use your selected action ID

6. Start Script

    - Run the `example-do-action.ahk` script


    ::success
    <kbd>F12</kbd> and <kbd>F11</kbd> _(or your updated hotkey combinations)_ should now execute your selected actions!
    ::


## Tips & Tricks

- You can easily create your own new scripts from scratch by simply including the core `lib/streamerbot.ahk` file from any new `.ahk` script!
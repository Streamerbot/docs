---
title: MacOS Support
description: Install Streamer.bot on MacOS
navigation: false
icon: i-mdi-apple
---

::callout{icon=i-mdi-alert color=amber}
Streamer.bot on MacOS is **experimental** and not officially supported.
::

## Introduction
Streamer.bot can be installed on MacOS using [Whisky](https://getwhisky.app)

- `winetricks` under `Run Winetricks Command`{lang=bash}
  - `dotnet48`
  - `d3dcompiler_47`
  - `dxvk`
  - `corefonts` *optional*
    - May be needed if you have issues launching Streamer.bot
  - `sapi` *optional*
    - Needed for Speaker.bot support

### Prerequisites

  1. Install `Whiskey`

    ::callout{icon=i-mdi-bookmark to="https://getwhisky.app"}
    Download and run the latest version of Whisky [here](https://getwhisky.app)
    ::

    2. Click `Winetricks` and run the following `Run Winetricks Command`s
 - Under `Fonts` select `corefonts` and click `Run`
    ![corefonts](/streamerbot/1.get-started/assets/corefonts.png)
    - Under `DLLs` select the following and click `Run` after each:
      - `sapi`
![sapi](/streamerbot/1.get-started/assets/sapi.png)
      - `dxvk`
  ![dxvk](/streamerbot/1.get-started/assets/dxvk.png)
      - `d3dcompiler_47` (Should auto install with `dxvk` but doesn't hurt to run this run just in case.)
      - `dotnet48` (This will take a bit to install.)
    ![dotnet48](/streamerbot/1.get-started/assets/dotnet48.png)

### Install
    1. Download Streamer.bot [here](https://streamer.bot) and MacOS should unpack it automatically.
    2. Click `Open C: Drive` and drag the Streamer.bot folder into `drive_c`.
    3. Click `Pin Program` and set `Pin name:` as Streamer.bot and select the Streamer.bot executable under `Program path:` by clicking `Browse`.
  ![pin-program](/streamerbot/1.get-started/assets/pin-program.png)

You should now see Streamer.bot in Whisky and be able to double click the icon to run it.
  ![sb-in-whisky](/streamerbot/1.get-started/assets/sb-in-whisky.png)

#### Update
Streamer.bot [Automatic Updates](/get-started/installation#automatic-updates) should work as usual.

You can manually update your Streamer.bot installation by downloading the latest version and copying the files into your existing install overwriting everything but the folders.

#### Uninstall
You can remove the Streamer.bot installation by right clicking the `Bottle` name and selecting `Remove`.

## Known Issues

### Groups
[Action](/guide/actions) and [Command](/guide/commands) lists do not render any configured group names or groupings.

All actions and commands are listed in the order they have been added.

### Viewer Context Menu
The :shortcut{value="Right-Click"} context menu on users within the viewers tab may not render correctly. You need to move the mouse over the opening context menu to let it fully appear.

::callout{icon=i-mdi-check color=green}
This issue has been resolved in Wine 7 and later
::

### Streamer.bot Chat
The built-in chat and event feed windows will not work due to missing `WebView2`.
---
title: Linux Support
description: Install Streamer.bot on Linux
navigation: false
icon: i-mdi-linux
---

::warning
Streamer.bot on Linux is **experimental** and not officially supported.
::

## Introduction
Streamer.bot can be installed on Linux using `wine` and `winetricks`

- `wine` `>= 6.19`{lang=bash}
- `winetricks` `>= 20210206`{lang=bash}
  - `dotnet48`
  - `d3dcompiler_47`
  - `dxvk`
  - `corefonts` *optional*
    - May be needed if you have issues launching Streamer.bot
  - `sapi` *optional*
    - Needed for Speaker.bot support

## Installation
Select an installation method below:

::card-group
  ::card{title="Install Script" to=#install-script icon=i-mdi-bash}
  Install Streamer.bot and its Wine dependencies using a `bash` script
  ::
  ::card{title="Bottles" to=#bottles icon=i-mdi-bottle-wine}
  Install Streamer.bot with Bottles
  ::
  ::card{title="Lutris" to=#lutris icon=i-simple-icons-lutris}
  Install Streamer.bot with Lutris
  ::
::

### Install Script

::callout{icon=i-mdi-github to="https://github.com/Streamerbot/sb-linux-installer"}
View [Streamerbot/sb-linux-installer](https://github.com/Streamerbot/sb-linux-installer) on GitHub
::


::steps{level=4}
  #### Prerequisites
  Install the required dependencies for your Linux distribution

  ::tabs

    ::tabs-item{label=Ubuntu icon=i-simple-icons-ubuntu}
      1. Install `wine`
          ::read-more{to="https://wiki.winehq.org/Ubuntu"}
          Follow the instructions [here](https://wiki.winehq.org/Ubuntu) to install Wine on your version of Ubuntu
          ::

      2. Install `winetricks`
          ```bash [Terminal]
          sudo apt install winetricks
          sudo winetricks --self-update
          ```

      3. Install remaining dependencies
          ```bash [Terminal]
          sudo apt install git curl
          ```
    ::

    ::tabs-item{label=Arch icon=i-simple-icons-archlinux}

        ```bash [Terminal]
        # Install wine
        sudo pacman -S wine

        # Install winetricks
        sudo pacman -S winetricks

        # Install remaining dependencies
        sudo pacman -S git curl
        ```
    ::

  ::

  #### Install Streamer.bot

  ```bash [Terminal]
  # Clone the repository
  git clone https://github.com/Streamerbot/sb-linux-installer

  # Change directory
  cd ./sb-linux-installer

  # Execute the installer
  ./install.sh
  ```

  #### Launch Streamer.bot

  ::success
  You can now launch **Streamer.bot** using the created desktop shortcut!
  ::
::

### Bottles

::callout{icon=i-mdi-github to="https://github.com/bottlesdevs/programs/blob/main/Software/streamerbot.yml"}
View `streamerbot.yml` on GitHub.
::

::steps{level=4}

  #### Install Bottles

  Install [Bottles](https://usebottles.com/){target=_blank rel=noopener} on your Linux distribution if you haven't already.

  #### Create a new Bottle

  1. Click the `+` icon in the top left corner to create a new Bottle.
  2. Enter a name for your Bottle, e.g. `"Streamer.bot"`{lang=cs}
  3. Select `Custom` configuration
  4. Ensure `soda` is selected as the runner
  5. Click `Create` (leave everything else as-is)

      ![Create and configure a new Bottle for Streamer.bot](../assets/linux-bottles-new.png){width=500}

  #### Install Streamer.bot

  1. Select your newly created Bottle from the list
  2. Click on `Install Programs...`

      ![Install Programs in Bottles](../assets/linux-bottles-install-programs.png){width=500}

  3. Select `"StreamerBot"`{lang=cs} from the list of available programs

      ![Streamer.bot in the built-in Bottles installers listing](../assets/linux-bottles-installers.png){width=500}

      It may take some time for the installation to complete.

  #### Launch Streamer.bot

  Click the :icon{name=i-mdi-play} `Run` button to launch Streamer.bot from your Bottle

  ![Launch Streamer.bot](../assets/linux-bottles-launch.png){width=500}

  ::success
  You now have **Streamer.bot** installed on Linux via Bottles!
  ::

::

#### Bottles Tips & Tricks

::note
**Improve WebView2 Performance in Bottles**
- You can optionally change the runner to `Proton-GE` or `Proton-CachyOS` to improve the performance of the Streamer.bot Chat window, C# Code editor and any other WebView2 content.
- *Note that this may cause some graphical glitches in Streamer.bot*
::

### Lutris
::callout{icon=i-mdi-github to="https://raw.githubusercontent.com/Streamerbot/sb-linux-installer/main/lutris/streamerbot.yaml"}
Download `lutris/streamerbot.yaml` from GitHub
::

1. Click the `+` in Lutris and select `Install from a local install script`

    ![Lutris Add Game Dialog](../assets/lutris-add-game.png){width=600}

2. Select the `streamerbot.yaml` file (download link above)
3. Follow the installer steps to install Streamer.bot to your location of choice.
4. Launch Streamer.bot from Lutris!

## Known Issues

### Groups
[Action](/guide/actions) and [Command](/guide/commands) lists do not render any configured group names or groupings.

All actions and commands are listed in the order they have been added.

### Viewer Context Menu
The :kbd{value="Right-Click"} context menu on users within the viewers tab may not render correctly. You need to move the mouse over the opening context menu to let it fully appear.

::success
This issue has been resolved in Wine 7 and later
::

::tip
  The speed with which the context menu appears can be improved by redirecting `stdout` to `/dev/null`

  ```bash
  wine Streamer.bot.exe >/dev/null 2>&1
  ```
::

### Streamer.bot Chat
The built-in chat and event feed windows will not work due to missing `WebView2` when using the install script or the Lutris installer. However, they work when using Bottles's Streamer.bot installer.
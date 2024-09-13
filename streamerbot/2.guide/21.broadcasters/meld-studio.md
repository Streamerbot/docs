---
title: Meld Studio
description: Configure Streamer.bot to interact with your Meld Studio instances
logo: /img/icons/meld-studio.png
---

::callout{icon=i-mdi-warning color=amber to=/get-started/setup#meld-studio}
You must enable **Allow remote connections** under Advanced. Check out the [Get Started Guide](/get-started/setup#meld-studio) for details.
::

::callout{icon=i-mdi-navigation}
Navigate to **Stream Apps > Meld Studio** in Streamer.bot
::

![Meld Studio Configuration](assets/meld-studio.png)

## Configuration
To add a new connection, <kbd>Right-Click</kbd> anyhere in the panel area and select `Add`:

![Meld Studio Add Connection](assets/meld-studio-add-connection.png)

Configuration options are outlined below:

::field-group
  ::field{name=Name type=Text required}
  Enter any name or label to describe this Meld Studio instance, e.g. `Local Meld Studio`
  ::

  ::field{name=Host type=Text required default="127.0.0.1"}
  Enter the host address of your PC

  If Meld Studio is running on the same machine as Streamer.bot, keep `127.0.0.1`

  For multi-pc setups you can configure this with another LAN IP address, e.g. `192.168.1.10`
  ::

  ::field{name="Auto Connect on Startup" type=Toggle}
  Automatically connect to this Meld Studio instance when Streamer.bot starts up
  ::

  ::field{name="Reconnect on Disconnect" type=Toggle}
  Automatically reconnect to this Meld Studio instance when the connection is disrupted
  ::

  ::field{name="Retry Interval" type=Number default=30}
  Change the interval of reconnection attempts when `Reconnect on Disconnect` is enabled
  ::
::

## Context Menu
<kbd>Right-Click</kbd> on a configured connection to reveal the context menu:

#### `Add`
Add a new Meld Studio connection

#### `Edit`
Edit the selected Meld Studio connection

#### `Delete`
Delete the selected Meld Studio connection

#### `Auto Connect`
Quickly toggle the `Auto Connect on Startup` configuration option for the selected connection

#### `Reconnect`
Quickly toggle the `Reconnect on Disconnect` configuration option for the selected connection

#### `Default`
Set this connection as the default when importing actions

::tip{color=amber}
If no default is set, imported actions will default to the first connection in the list
::

#### `Force`
Temporarily override **all** Meld Studio connections to use the selected connection.

::callout{icon=i-mdi-alert color=amber}
This setting does **not** persist when you restart Streamer.bot
::

#### `Update All Actions To...`
Reconfigure all actions utilizing an Meld Studio connection to use the selected connection

#### `Connect`
Manually attempt to connect to the selected connection

## Status Panel
Selecting a connected Meld instance in the left panel will reveal additional realtime information about that instance on the right panel.

#### `Current Scene`
Shows the name of the currently broadcasting scene on the selected connection

#### `Stream Status`
Shows the status of the current streaming and recording activity

#### `Scenes/Layers`
Lists all layers present on the currently selected scene

## Usage
:api-reference-cards{path=meld-studio}
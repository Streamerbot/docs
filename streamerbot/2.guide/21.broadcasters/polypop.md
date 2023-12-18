---
title: PolyPop
description: Integrate Streamer.bot with PolyPop
logo: /img/icons/polypop.png
---

PolyPop integration is made possible via the community-made Websocket plugin available from `Plugins` in PolyPop:

Click on the `Plugins` button in the top-left corner in PolyPop

![PolyPop Plugins Button](assets/polypop-plugins.png)

In this menu nevagate to the `Web Services` tab, and install the Websockets plugin

![PolyPop Websocket Plugin](assets/polypop-websockets-plugin.png)

---

::callout{icon=i-mdi-navigation}
Navigate to **Stream Apps > PolyPop**
::

![PolyPop Configuration](assets/polypop.png)

## Configuration
::field-group
  ::field{name="Auto Start" type=Toggle}
  Automatically connect to PolyPop when Streamer.bot starts up
  ::

  ::field{name=Address type=Text required default="127.0.0.1"}
  Enter the host address of your PolyPop Websocket Plugin

  - Default: `127.0.0.1`
  ::

  ::field{name=Port type=Number required default="9652"}
  - Default: `9652`
  ::

  ::field{name=Endpoint type=Text required default="/"}
  - Default: `/`
  ::
::


## Usage
::callout{icon=i-mdi-bookmark color=green to=/api/sub-actions/polypop/trigger-alert}
Explore all **PolyPop sub-actions** and their variables at [API References > Sub-Actions > PolyPop](/api/sub-actions/polypop/trigger-alert)
::
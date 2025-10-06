---
title: DoAction (UDP)
navigation.title: DoAction
description: Trigger an action in Streamer.bot via UDP
icon: mdi:api
navigation.icon: mdi:api
---

## `DoAction`
Execute an action on the Streamer.bot instance

::code-group
  ```json [↗️ Request Format]
  {
    "request": "DoAction",
    "action": {
      "id": "<guid>",
      "name": "<name>"
    },
    "args": {
      "key": "value"
    }
  }
  ```
::

::tip
You can specify either one of the action `id` or `name`, you do not need both.
::
# Application
Streamer.bot application events emitted by the WebSocket Server

## Overview
You can enable `Application` events with this [Subscribe](/api/servers/websocket/requests#subscribe) request:

```json [Subscribe Request]
{
  "request": "Subscribe",
  "id": "my-subscribe-id",
  "events": {
    "Application": [
      "ActionAdded",
      "ActionUpdated",
      "ActionDeleted"
    ]
  },
}
```

## Events
### `ActionAdded`
Emitted when a new action is created in Streamer.bot

::code-group
  ```ts [JSON Schema]
  {
    id: string;
    name: string;
    group: string;
    enabled: boolean;
  }
  ```
  ```json [Example]
  {
    "id": "9ed46f4e-a76b-4a1a-92b7-0a12a78a2c3a",
    "name": "Test Action",
    "group": "",
    "enabled": true
  }
  ```
::

### `ActionUpdated`
Emitted when an action is modified in Streamer.bot

::code-group
  ```ts [JSON Schema]
  {
    id: string;
    name: string;
    group: string;
    enabled: boolean;
  }
  ```
  ```json [Example]
  {
    "id": "9ed46f4e-a76b-4a1a-92b7-0a12a78a2c3a",
    "name": "Test Action",
    "group": "Group",
    "enabled": true
  }
  ```
::


### `ActionDeleted`
Emitted when an action has been deleted in Streamer.bot

::code-group
  ```ts [JSON Schema]
  {
    id: string;
    name: string;
    group: string;
    enabled: boolean;
  }
  ```
  ```json [Example]
  {
    "id": "9ed46f4e-a76b-4a1a-92b7-0a12a78a2c3a",
    "name": "Test Action",
    "group": "Group",
    "enabled": true
  }
  ```
::
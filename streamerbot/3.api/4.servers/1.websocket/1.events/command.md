---
navigation.title: Command
---

# Command Events
All command related events emitted by the WebSocket Server

## Overview
You can enable `Command` events with this [Subscribe](/api/servers/websocket/requests#subscribe) request:

```json [Subscribe Request]
{
  "request": "Subscribe",
  "id": "my-subscribe-id",
  "events": {
    "Command": [
      "Message",
      "Whisper",
      "BotWhisper",
      "MessageCooldown",
    ]
  },
}
```

## Events
### `Message`
```json
{
  "command": "!bots",
  "counter": 1,
  "userCounter": 1,
  "message": "",
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": true,
    "role": 4
  }
}
```

### `Whisper`
```json
{
  "command": "!bots",
  "counter": 1,
  "userCounter": 1,
  "message": "",
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": true,
    "role": 4
  }
}
```

### `BotWhisper`
```json
{
  "command": "!bots",
  "counter": 1,
  "userCounter": 1,
  "message": "",
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": true,
    "role": 4
  }
}
```

### `MessageCooldown`
```json
{
  "command": "!bots",
  "cooldownLeft": 11,
  "globalCooldownLeft": 11,
  "userCooldownLeft": 0,
  "message": "",
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": false,
    "role": 1
  }
}
```
---
title: UDP Broadcast
description: Broadcast a UDP payload to a specific port
parameters:
  - name: UDP Port
    required: true
    type: Number
    description: Port of the UDP server to broadcast to
  - name: Payload Data
    required: true
    type: Text
    description: |
      Enter the data to send to the UDP server

      For example, this could be simple text strings, or structured text such as JSON.

      Refer to the documentation of the UDP interface you are interacting with.

      Example payloads:
      ::code-group
        ```json[Speaker.bot UDP Server]
        {
          "command": "speak",
          "id": "1234",
          "voice": "BotVoice",
          "message": "It's %user%"
        }
        ```
        ```[RetroArch Command Interface]
        FAST_FORWARD
        ```
      ::
---
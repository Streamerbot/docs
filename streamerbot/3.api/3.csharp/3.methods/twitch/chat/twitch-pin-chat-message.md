---
name: TwitchPinChatMessage
title: TwitchPinChatMessage
description: Pins a chat message in Twitch
version: 1.0.5
parameters:
  - name: messageId
    description: Twitch chat message ID to pin
  - name: duration
    default: null
    description: |
      The duration to pin the chat message for.
      - `null` for the pin to last till the end of the stream
      - between `30` and `1800` - duration in seconds
example: |
  using System;
  public class CPHInline
  {
      public bool Execute()
      {
          // get the message id from an argument
          if (!CPH.TryGetValue<string>("msgId", out var msgId))
          {
              return false;
          }

          // pin the chat message till the end of the stream
          CPH.TwitchChatPinChatMessage(msgId);

          return true;
      }
  }
---

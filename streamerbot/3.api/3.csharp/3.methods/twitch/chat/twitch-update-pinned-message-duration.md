---
name: TwitchUpdatePinnedMessageDuration
title: TwitchUpdatePinnedMessageDuration
description: Update the duration of a pinned chat message
version: 1.0.5
parameters:
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
          // update the pinned chat message to show for 60 seconds
          CPH.TwitchUpdatePinnedMessageDuration(60);

          return true;
      }
  }
---

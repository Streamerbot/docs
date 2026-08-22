---
name: TwitchUnpinMessage
title: TwitchUnpinMessage
description: Unpin the pinned chat message
version: 1.0.5
example: |
  using System;
  public class CPHInline
  {
      public bool Execute()
      {
          // unpin the pinned chat message
          CPH.TwitchUnpinMessage();

          return true;
      }
  }
---

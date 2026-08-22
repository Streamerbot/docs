---
name: KickDeleteChatMessage
title: KickDeleteChatMessage
description: Deletes the selected chat message (by message ID) from the Kick stream
version: 1.0.7
example: |
  using System;
  public class CPHInline
  {
      public bool Execute()
      {
          // get the current messaged ID from the Kick chat message
          CPH.TryGetArg("messageId", out string messageId);

          // delete the associated Kick chat message
          CPH.KickDeleteChatMessage(messageId);

          return true;
      }
  }
---
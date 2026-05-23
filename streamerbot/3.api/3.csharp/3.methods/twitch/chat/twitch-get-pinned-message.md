---
name: TwitchGetPinnedMessage
title: TwitchGetPinnedMessage
description: Gets the current pinned chat message
version: 1.0.5
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            // get the current pinned chat message
            var pinnedMessage = CPH.TwitchGetPinnedMessage();

            return true;
        }
    }
---

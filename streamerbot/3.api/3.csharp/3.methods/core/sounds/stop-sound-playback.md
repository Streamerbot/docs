---
name: StopSoundPlayback
title: StopSoundPlayback
description: Stops the currently playing sound from Streamer.bot, by name
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Stop all sounds with the name "Kachow"
            CPH.StopSoundPlayback("Kachow");
            
            return true;
        }
    }
---

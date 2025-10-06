---
name: CommandSetUserCooldownDuration
title: CommandSetUserCooldownDuration
description: Set the user cooldown duration of a command, by ID
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define string of commandId
            string commandId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";

            //Set global cooldown to 42 seconds
            CPH.CommandSetUserCooldownDuration(commandId, 42);
            
            return true;
        }
    }
---

---
description: Will add time(seconds) to current global cooldown of a command, by ID
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define string of commandId
            string commandId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            
            //Add cooldown to current running global cooldown of command
            CPH.CommandAddToGlobalCooldown(commandId, 42);
            
            return true;
        }
    }
---

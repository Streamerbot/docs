---
name: CommandRemoveAllUserCooldowns
title: CommandRemoveAllUserCooldowns
description: Remove all user cooldowns associated with the specified command, by ID
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define string of commandId
            string commandId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            
            //Remove all user cooldowns
            CPH.CommandRemoveAllUserCooldowns(commandId);
            
            return true;
        }
    }
---

---
name: CommandResetGlobalCooldown
title: CommandResetGlobalCooldown
description: Resets global cooldown of command, by ID
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define string of commandId
            string commandId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            
            //Set global cooldown back to start
            CPH.CommandResetGlobalCooldown(commandId);
            
            return true;
        }
    }
---

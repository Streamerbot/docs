---
name: DisableCommand
title: DisableCommand
description: Disables a command, by ID
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            // Specify id of command you want to disable
            string commandId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            
            //Disable command by id
            CPH.DisableCommand(commandId);
            
            return true;
        }
    }
---

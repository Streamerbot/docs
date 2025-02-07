---
description: Enables a command, by ID
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            // Specify id of command you want to enable
            string commandId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            
            //Enable command by id
            CPH.EnableCommand(commandId);
            
            return true;
        }
    }
---

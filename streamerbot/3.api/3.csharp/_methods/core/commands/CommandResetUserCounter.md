---
description: Resets the total counter for a specified user for the given command, by ID
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define string of commandId
            string commandId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            //Get current user id
            CPH.TryGetArg("userId",out string userId);
            //Get current platform of user
            CPH.TryGetArg("userType",out string userType);
            Enum.TryParse(userType, out Platform platform);
            
            //Reset CommandUserCounter
            CPH.CommandResetUserCounter(commandId, userId, platform);
            
            return true;
        }
    }
---

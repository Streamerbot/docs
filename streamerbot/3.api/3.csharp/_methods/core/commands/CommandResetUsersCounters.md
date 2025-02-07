---
description: Resets the total counter for all users of a platform for the given command, by ID
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define string of commandId
            string commandId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";

            //Define Platform only "twitch", "youtube", "trovo"
            Enum.TryParse("twitch", out Platform platform);
            
            //Reset all persisted user counters
            CPH.CommandResetUsersCounters(commandId, platform, true);
            
            return true;
        }
    }
---

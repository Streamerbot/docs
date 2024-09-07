---
description: Check if an action exist by name<br>Returns a boolean indicating whether the action exists.
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Set action name which you want to check
            string actionName = "Streamer.bot Docs Action";

            //Get True or False whether action exists or not
            bool exists = CPH.ActionExists(actionName);

            return true;
        }
    }
---

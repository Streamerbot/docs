---
description: Run an action, by id<br>Returns a boolean indicating whether the operation was successful.
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Specify name of action you want to run
            string actionId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            
            //Run Action (in current queue)
            CPH.RunAction(actionId);
            CPH.RunAction(actionId, true);
            
            //Run Action in it's own queue
            CPH.RunAction(actionId, false);
            
            return true;
        }
    }
---

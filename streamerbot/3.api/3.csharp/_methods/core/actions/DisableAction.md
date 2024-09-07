---
description: Disables an action, by name
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get action name
            CPH.TryGetArg("actionName",out string actionName);
            
            //Disable action by name
            CPH.DisableAction(actionName);
            
            return true;
        }
    }
---

---
description: Disables an action, by ID
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get action id of current action 0.2.5
            CPH.TryGetArg("actionId",out string actionId);
            
            //Get action id of current action pre 0.2.5
            //CPH.TryGetArg<Guid>("actionId", out var actionIdVar);
            //string actionId = actionIdVar.ToString();
            
            CPH.DisableActionById(actionId);
            return true;
        }
    }
---

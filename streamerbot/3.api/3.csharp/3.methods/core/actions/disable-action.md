---
name: DisableAction
title: DisableAction
description: Disables an action, by name
example: |
    using System;

    public class CPHInline
    {
        public bool Execute()
        {
            // Get current action name
            CPH.TryGetArg("actionName", out string actionName);

            // Disable action by name
            CPH.DisableAction(actionName);

            return true;
        }
    }
---

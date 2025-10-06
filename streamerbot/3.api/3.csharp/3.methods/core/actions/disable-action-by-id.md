---
name: DisableActionById
title: DisableActionById
description: Disables an action, by ID
version: 0.2.4
example: |
    using System;

    public class CPHInline
    {
        public bool Execute()
        {
            // Get action id of current action
            CPH.TryGetArg("actionId",out string actionId);

            CPH.DisableActionById(actionId); // [!code highlight]

            // test

            return true;
        }
    }
---

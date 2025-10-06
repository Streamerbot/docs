---
name: EnableAction
title: EnableAction
description: Enables an action, by name
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Set action name you want to enable
            string actionName = "Streamer.bot Docs Action";
            
            //Enable action by name
            CPH.EnableAction(actionName);
            
            return true;
        }
    }
---

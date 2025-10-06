---
name: GetActions
title: GetActions
description: Returns a list of action data for all available actions
version: 0.2.4
example: |
    using System;
    using System.Collections.Generic;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get list of actions
            List<ActionData> actionList = CPH.GetActions();
            
            //Example to go through list and write them to logfile
            foreach(ActionData action in actionList)
            {
                //Get id of current action var.
                //Due to it being Guid type need to convert to string.
                string id = action.Id.ToString();
                //Get name of current action var
                string name = action.Name;
                //Write to log
                CPH.LogInfo($"ActionId:{id}, Action Name: {name}");
            }
            return true;
        }
    }
---

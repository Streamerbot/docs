---
name: EnableActionById
title: EnableActionById
description: Enables an action, by ID
version: 0.2.4
parameters:
  - name: actionId
    default: '"1234-abcde-5678"'
    description: |
      You can get the action id by right-clicking on an action and `Copy Action Id`
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define action id you want to enable
            string actionId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            
            CPH.EnableActionById(actionId);
            return true;
        }
    }
---

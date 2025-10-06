---
name: GetGlobalVar
title: GetGlobalVar
description: Fetch a global variable by name
parameters:
  - import: GlobalVarName
  - import: GlobalPersisted
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Examples on usage
            //Get integer number from persisted global variable
            int myInt = CPH.GetGlobalVar<int>("myInt");

            //Get string/text from persisted global variable
            string myString = CPH.GetGlobalVar<string>("myString",true);

            //Get string/text from non-persisted global variable
            string myString = CPH.GetGlobalVar<string>("myString",false);

            return true;
        }
    }
---

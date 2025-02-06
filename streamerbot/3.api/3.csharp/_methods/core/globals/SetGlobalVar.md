---
description: Set the value for a global variable
parameters:
  - import: GlobalVarName
  - import: GlobalPersisted
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
			string value = "This is saved to a global variable";
            
            //Examples on usage
            //Save to a persisted global variable called "myString"
			CPH.SetGlobalVar("myString", value, true);
            
			//Save to a non-persisted global variable called "myString"
            CPH.SetGlobalVar("myString", value, false);
            
            return true;
        }
    }
---
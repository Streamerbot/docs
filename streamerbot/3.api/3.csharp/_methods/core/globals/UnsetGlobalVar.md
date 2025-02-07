---
description: Remove a global variable by name
parameters:
  - import: GlobalVarName
  - import: GlobalPersisted
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Please be extremely careful with this method
            //Only possible to restore with back-up

            //Unset persisted global variable "myString"
            CPH.UnsetGlobalVar("myString");
            CPH.UnsetGlobalVar("myString", true);

            //Unset non-persisted global variable "myString"
            CPH.UnsetGlobalVar("myString", false);

            return true;
        }
    }
---
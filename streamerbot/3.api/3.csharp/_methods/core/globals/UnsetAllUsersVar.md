---
description: Unset a user variable for **all** users
version: 0.2.1
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

            //Unset all(!) persisted user variable called "myString"
            CPH.UnsetAllUsersVar("myString");
            CPH.UnsetAllUsersVar("myString", true);

            //Unset all(!) non-persisted user variable called "myString"
            CPH.UnsetAllUsersVar("myString", false);
            return true;
        }
    }
---
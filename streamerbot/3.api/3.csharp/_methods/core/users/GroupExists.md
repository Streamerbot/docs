---
description: Returns bool verifying existence of a group, by name
version: 0.2.4
parameters:
  - import: UserGroupName
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define the groupname you want to check
            string groupName = "Test Group";

            //Method returns a bool type which you can check if the group exists
            bool groupExists = CPH.GroupExists(groupName);
            return true;
        }
    }
---

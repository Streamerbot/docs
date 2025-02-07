---
description: Creates a new group with the given name
version: 0.2.4
parameters:
  - import: UserGroupName
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define the groupname you want to create
            string groupName = "Test Group";
            
            //Method returns a bool type which you can check if the group was added
            bool gotAdded = CPH.AddGroup(groupName);
            return true;
        }
    }
---

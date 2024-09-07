---
description: Remove all users from a group
version: 0.2.3
parameters:
  - import: UserGroupName
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define the groupname you want to clear
            string groupName = "Test Group";

            //Method returns a bool indicating the success of clearing the group
            bool usersCleared = CPH.ClearUsersFromGroup(groupName);
            return true;
        }
    }
---
---
description: Remove a user, by username, from a group
version: 0.2.3
parameters:
  - import: UserName
  - import: Platform
  - import: UserGroupName
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define the groupname you want to add the user to
            string groupName = "Test Group";
            //Get userName of current user
            CPH.TryGetArg("userName",out string userName);

            //Method returns a bool type which you can check if the user was removed
            bool userGotRemoved = CPH.RemoveUserFromGroup(userName, Platform.Twitch, groupName);
            return true;
        }
    }
---
---
description: Add a user, by username, to a group
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
            //Get UserName
            CPH.TryGetArg("userName",out string userName);

            //Method returns a bool type which you can check if the user was added
            bool userGotAdded = CPH.AddUserToGroup(userName, Platform.Twitch, groupName);
            return true;
        }
    }
---
---
description: Add a user, by ID, to a group
version: 0.2.3
parameters:
  - import: UserId
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
            //Get UserId
            CPH.TryGetArg("userId",out string userId);

            //Method returns a bool type which you can check if the user was added
            bool userGotAdded = CPH.AddUserIdToGroup(userId, Platform.Twitch, groupName);
            return true;
        }
    }
---
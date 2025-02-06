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
            
            //Get user type and define the Platform Enum
            CPH.TryGetArg("userType",out string userType);
            Enum.TryParse(userType, out Platform platform);

            //Method returns a bool type which you can check if the user was added
            bool userGotAdded = CPH.AddUserIdToGroup(userId, platform, groupName);
            return true;
        }
    }
---
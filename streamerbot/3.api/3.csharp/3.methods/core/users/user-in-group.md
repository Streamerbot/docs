---
name: UserInGroup
title: UserInGroup
description: Check if a user, by username (login name), is a member of a group
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
            
            //Get user type and define the Platform Enum
            CPH.TryGetArg("userType",out string userType);
            Enum.TryParse(userType, out Platform platform);

            //Method returns a bool type which you can check if the user is in group
            bool userInGroup = CPH.UserInGroup(userName, platform, groupName);
            return true;
        }
    }
---
---
name: RemoveUserFromGroup
title: RemoveUserFromGroup
description: Remove a user, by username (login name), from a group
version: 0.2.3
parameters:
  - name: userName
    import: core/users/username
  - name: platform
    import: core/platform
  - name: groupName
    import: core/users/group-name
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

            //Method returns a bool type which you can check if the user was removed
            bool userGotRemoved = CPH.RemoveUserFromGroup(userName, platform, groupName);
            return true;
        }
    }
---
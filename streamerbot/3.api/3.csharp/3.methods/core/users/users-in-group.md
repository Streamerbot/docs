---
name: UsersInGroup
title: UsersInGroup
description: Fetch a list of users in a group
version: 0.2.3
parameters:
  - name: groupName
    import: core/users/group-name
example: |
    using System;
    using System.Collections.Generic;//due to List usage
    public class CPHInline
    {
        public bool Execute()
        {
            //Define the groupname you want to add the user to
            string groupName = "Test Group";

            //Get List of GroupUsers
            List<GroupUser> groupUsers = CPH.UsersInGroup(groupName);

            //Write each user of group into logs example
            foreach(GroupUser userInfo in groupUsers)
            {
                //user name of current user
                string user = userInfo.Username;
                //platform type of current user
                string userType = userInfo.Type;

                CPH.LogInfo($"Username: {user}, Platform: {userType}");
            }
            return true;
        }
    }
---
---
description: Deletes the group matching the provided name
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define the groupname you want to delete
            string groupName = "Test Group";

            //Method returns a bool type which you can check if the group was deleted
            bool groupDeleted = CPH.DeleteGroup(groupName);
            return true;
        }
    }
---

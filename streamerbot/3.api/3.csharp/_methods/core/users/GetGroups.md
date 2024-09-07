---
description: Returns a list of all available groups
version: 0.2.4
example: |
    using System;
    using System.Collections.Generic;//due to List usage
    public class CPHInline
    {
        public bool Execute()
        {
            //Get a list of group names
            List<string> groupList = CPH.GetGroups();

            //Write each group name into logs example
            foreach(string group in groupList)
            {
                CPH.LogInfo($"GroupName: {group}");
            }
            return true;
        }
    }
---

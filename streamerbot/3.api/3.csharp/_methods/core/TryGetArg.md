---
description: Load an [argument](/guide/variables) and parse it into a C# variable type
version: 0.2.3
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //OptionA
            CPH.TryGetArg<string>("userName",out string userName);
            
            //OptionB
            //Check whether userId argument exists directly as TryGetArg returns boolean
            if( CPH.TryGetArg("userId",out string userId) )
            {
                //Do things if userId existed
                string test = "UserId:" + userId;
            }
            
            return true;
        }
    }
---

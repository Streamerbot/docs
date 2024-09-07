---
description: Set an [argument](/guide/variables) to be used in subsequent sub-actions
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Have a variable you want to set as argument
            string test = "This is a test";

            //Set the argument name and value of argument
            CPH.SetArgument("testArgument", test);
            
            return true;
        }
    }
---
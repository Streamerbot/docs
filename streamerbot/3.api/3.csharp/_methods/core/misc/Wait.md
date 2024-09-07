---
description: Will make the code wait for specified amount of time, in ms
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            CPH.SendMessage("This is the first message.");
            
            //Wait 5 seconds
            CPH.Wait(5000);
            
            CPH.SendMessage("This is the second message.");
            return true;
        }
    }
---
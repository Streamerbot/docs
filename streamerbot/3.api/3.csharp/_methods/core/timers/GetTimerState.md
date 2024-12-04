---
description: Get the state of an existing timer
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define timer id you want to get the state of
            string timerId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            
            //Methods return boolean indicating if timer enabled or not
            bool state = CPH.GetTimerState(timerId);
            return true;
        }
    }
---
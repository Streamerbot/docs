---
description: Set the interval of an existing timer, in seconds
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define timer id you want to set the interval of
            string timerId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            //Set the wanted interval for example 10
            int newInterval = 10;
            
            //Set the timer interval with method
            CPH.SetTimerInterval(timerId, newInterval);
            
            return true;
        }
    }
---
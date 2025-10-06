---
name: Between
title: Between
description: Returns a random int value between(including) min and max
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get an int value between 1 and 100
            int randomInt = CPH.Between(1,100);
            //Set the argument called randomNum to the value of randomInt
            CPH.SetArgument("randomNum",randomInt);
            
            return true;
        }
    }
---

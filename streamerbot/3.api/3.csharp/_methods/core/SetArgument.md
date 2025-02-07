---
description: Set an [argument](/guide/variables) to be used in subsequent sub-actions
parameters:
  - name: variableName
    required: true
    description: Name of the argument you are assigning a value to
    default: '"myArgName"'
  - name: value
    required: true
    description: Value assigned to the argument
    default: '"Hello World!"'
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
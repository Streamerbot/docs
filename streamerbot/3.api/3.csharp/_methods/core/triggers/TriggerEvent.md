---
description: Trigger custom events that are defined with the [Custom Event Trigger](api/triggers/custom/custom)
version: 0.2.0
parameters:
  - name: eventName
    type: string
    required: true
    description: |
      Name of the custom event trigger defined with a UI custom trigger
  - name: useArgs
    type: bool
    required: false
    description: |
      Forward the currently available arguments to the custom trigger
    default: true
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define the eventName 
            string eventName = "SB_Docs_Trigger";

            //Fire the custom event trigger by eventName and
            //sending the current available arguments to it
            CPH.TriggerEvent(eventName, true)
            
            return true;
        }
    }
---
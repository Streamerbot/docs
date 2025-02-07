---
description: Register a custom trigger
version: 0.2.0
parameters:
  - name: triggerName
    type: string
    required: true
    description: |
      Name of the trigger shown in the context menu
  - name: eventName
    type: string
    required: true
    description: |
      Define the name of the event for later use in [TriggerCodeEvent](/api/csharp/core/triggers#TriggerCodeEvent) method
  - name: categories
    type: String[]
    required: true
    description: |
      Define the categories in the context menu in which the trigger will be shown
example: |
    using System;
    public class CPHInline
    {
        public void Init()
        {
          // Preferably Custom Triggers are registered during initialization of the code instance
          // Often in combination with Pre-Compile on Application start in the Execute-Code settings

          //Define the categories in custom trigger menu
          string[] categories = {"Streamer.bot","Documentation"};


          //Define the event name for later usage in code with CPH.TriggerCodeEvent(eventName)
          //Advise on making it fairly unique names to your code/extension
          string eventName = "sbDocsUpdate";

          //Register custom trigger. Will give boolean result if successfull
          bool success = CPH.RegisterCustomTrigger(triggerName, eventName, categories);
        }

        public bool Execute()
        {
            // Custom Trigger can also be registered with Execute but common usage is
            // in the Init() method as shown above
            return true;
        }
    }
---
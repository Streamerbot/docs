---
description: Pause a specific action queue by name
parameters:
  - name: name
    default: '"SoundAlerts"'
    description: Name of your action queue
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define the name of the queue you want to pause
            string queueName = "SoundAlerts";

            //Pause Action Queue
            CPH.PauseActionQueue(queueName);

            return true;
        }
    }
---

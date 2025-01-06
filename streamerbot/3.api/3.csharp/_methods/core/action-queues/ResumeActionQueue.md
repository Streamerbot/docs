---
description: Resume action queue, optionally clear all pending actions before resume
parameters:
  - name: name
    default: '"SoundAlerts"'
    description: Name of your action queue
  - name: clear
    default: false
    description: |
      - `true`{lang=cs} - Clear still pending actions in queue before resume
      - `false`{lang=cs} - Do not clear pending actions in queue
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define the name of the queue you want to pause
            string queueName = "SoundAlerts";
            //Define if current pending actions should be cleared
            bool clear = false;

            //Resume specific queue
            CPH.ResumeActionQueue(queueName,clear);

            return true;
        }
    }
---

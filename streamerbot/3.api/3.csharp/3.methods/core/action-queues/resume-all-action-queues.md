---
name: ResumeAllActionQueues
title: ResumeAllActionQueues
description: Resume all paused queues, optionally clear all pending actions before resume
parameters:
  - name: clear
    default: false
    description: |
      - `true`{lang=cs} - Clear still pending actions in the paused queues before resume
      - `false`{lang=cs} - Do not clear pending actions in paused queues
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define if current pending actions should be cleared
            bool clear = false;

            //Resume specific queue
            CPH.ResumeAllActionQueues(clear);

            return true;
        }
    }
---

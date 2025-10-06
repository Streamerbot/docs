---
name: RunAction
title: RunAction
description: |
    Run an action, by name

    Returns a boolean indicating whether the operation was successful.
parameters:
  - name: runImmediately
    default: true
    description: |
      - `true`  - Will run the action as part of the current action, like a sub-action
      - `false` - Will run the action in it's own set queue. Code will continue without waiting
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            // Specify name of action you want to run
            string actionName = "Streamer.bot Docs Action";

            // Run Action (in current queue)
            CPH.RunAction(actionName);
            CPH.RunAction(actionName, true);

            // Run Action in it's own queue
            CPH.RunAction(actionName, false);

            return true;
        }
    }
---

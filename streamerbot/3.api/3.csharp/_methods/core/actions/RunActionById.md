---
description: |
    Run an action, by id

    Returns a boolean indicating whether the operation was successful.
parameters:
  - name: runImmediately
    default: true
    description: |
      - `true`  - Will run the action as part of the current action, like a subaction
      - `false` - Will run the action in it's own set queue. Code will continue without waiting
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            // Specify id of action you want to run
            string actionId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";

            // Run Action (in current queue)
            CPH.RunActionById(actionId);
            CPH.RunActionById(actionId, true);

            // Run Action in it's own queue
            CPH.RunActionById(actionId, false);

            return true;
        }
    }
---

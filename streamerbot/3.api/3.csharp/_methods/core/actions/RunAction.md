---
description: |
    Run an action, by name

    Returns a boolean indicating whether the operation was successful.
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

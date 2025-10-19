---
name: RunAction
title: RunAction
description: Execute another Streamer.bot action
parameters:
  - name: runImmediately
    default: true
    description: Whether to run the action immediately, inline with the current action, or in it's own queue
    options:
      - value: true
        description: Will run the action as part of the current action, like a sub-action
      - value: false
        description: Will run the action in it's own set queue. Code will continue without waiting
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

  Run an action, by name

  Returns a boolean indicating whether the operation was successful.
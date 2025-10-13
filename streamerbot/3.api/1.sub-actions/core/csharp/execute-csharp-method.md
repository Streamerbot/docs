---
title: Execute C# Method
description: Execute a custom method defined in another Execute C# Code sub-action
parameters:
  - name: Execute C# Code
    type: Select
    required: true
    description: |
      Select the [`Execute C# Code`](/api/sub-actions/core/csharp/execute-csharp-code) sub-action instance you would like to reference.

      ::warning
      You must configure the `Name` field in your `Execute C# Code` sub-action settings to display it here. [Read more >](/api/sub-actions/core/csharp/execute-csharp-code#configuration)
      ::
  - name: Method
    type: Select
    required: true
    description: |
      Select the method to execute

      ::tip
      This can be any custom defined method, or even the main `Execute()`{lang=cs} method.
      ::
  - name: Run on UI Thread
    type: Toggle
    default: false
    description: |
      Whether to run the method on the UI thread. This is useful if your method is spawning UI elements.
  - name: Save Result to Variable
    type: Toggle
    default: false
    description: |
      Whether to save the `bool`{lang=cs} result of the method to a variable

      ::warning
      **This changes the default behavior of the sub-action**
      <br>
      By default, a method returning `false`{lang=cs} will simply stop execution of the entire action.
      <br>
      Enabling this option allows you to collect the result and also continue execution **regardless of the return value**.
      ::
  - name: Variable Name
    type: Text
    description: When `Save Result to Variable`{color=primary} is enabled, define the name of the resulting variable.
---

Using this sub-action you can directly call into methods defined in any existing [Execute C# Code](/api/sub-actions/core/csharp/execute-csharp-code) sub-actions in your Streamer.bot instance.

:read-more{to=/api/csharp/guide/custom-methods}
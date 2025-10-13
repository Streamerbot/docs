---
title: Execute C# Code
description: Sub-action for writing advanced custom actions with C# code
parameters:
  - name: Name
    type: Text
    description: |
      Optionally set a descriptive name for your C# sub-action.

      ::tip
      `Name` is required if you would like to share custom methods with the [Execute C# Method](/api/sub-actions/core/csharp/execute-csharp-method) sub-action.
      ::
  - name: Description
    type: Text
    description: Optionally set a longer description detailing what your C# sub-action does.
  - name: Precompile on Application Start
    type: Toggle
    default: false
    description: By ticking this, your code will be automatically compiled when you start Streamer.bot so it is ready to go, instead of the first time the sub-action is executed.
  - name: Delayed Start
    type: Toggle
    default: false
    description: |
      When `Precompile on Application Start`{color=primary} is enabled, delay compilation until later in the startup routine.

      ::tip
      This is useful if you are **implementing UI** within your C# sub-action.
      ::
  - name: Save Result to Variable
    type: Toggle
    default: false
    description: |
      Save the `bool`{lang=cs} result of the `Execute()`{lang=cs} method

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

:read-more{to=/api/csharp/guide}
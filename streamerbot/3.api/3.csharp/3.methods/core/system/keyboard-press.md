---
name: KeyboardPress
title: KeyboardPress
description: Simulate a keyboard input
parameters:
  - name: keyPress
    type: string
    required: true
    description: |
      The keystroke to send.
example: |
    using System;

    public class CPHInline
    {
      public bool Execute()
      {
        // Examples:

        // 'W'
        CPH.KeyboardPress("{W}");

        // 'DOWN ARROW'
        CPH.KeyboardPress("{DOWN}");

        // 'SHIFT' and 'W'
        CPH.KeyboardPress("+{W}");

        // 'CTRL' and 'W'
        CPH.KeyboardPress("^{W}");

        // 'ALT' and 'W'
        CPH.KeyboardPress("%{W}");

        return true;
      }
    }
---

This CPH method uses the [SendKeys](https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.sendkeys.send) method.

The `keyPress` string argument needs to be enclosed in curly brackets `{}`.

To use key combinations such as :kbd{value="Shift"}, :kbd{value="meta"} and :kbd{value="Alt"}, you can use code modifiers listed in the link below.

::read-more{to="https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.sendkeys.send"}
Full reference of all [SendKeys](https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.sendkeys.send) keystroke values and modifiers.
::
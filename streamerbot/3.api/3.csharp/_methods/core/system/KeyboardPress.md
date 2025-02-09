---
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
    // The CPH method uses the SendKeys method. That means the keyPress string needs to be enclosed in curly brackets {}. To use key combinations (SHIFT, CTRL and ALT) you can use code modifiers listed in the link or the examples below.

    // https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.sendkeys.send

    // Note: The key list in the link above is exhaustive. If a key isn't listed there, then it's not available for this method.

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

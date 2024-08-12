---
title: Keyboard Press
description: Simulate key press events to the active application or trigger global hotkeys
parameters:
  - name: Key
    type: Select
    required: true
    description: |
      Choose the key to be pressed.

      _Not all possible keys are listed, as some just do not make sense at the moment. This list may be expanded in the future._

      ::warning
      Using fullscreen applications and/or running applications in administrator mode can prevent simulated key presses from working in that application.<br>
      We **do not** advocate running Streamer.bot in administrator mode as a fix.
      ::
  - name: Modifiers
    type: Toggle
    description: Choose any additional modifier keys to include with the key press
---

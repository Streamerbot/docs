---
title: Key Press
description: Trigger for hotkey combinations
version: 1.0.0
parameters:
  - name: Key Combination
    type: Text
    description: |
      Key combination for triggering this hotkey.

      ::tip
      Click `Capture Key` to capture a key combination
      ::
variables:
  - name: modifier
    type: number
    description:
    value: 11
  - name: hasCtrl
    type: bool
    description:
    value: True
  - name: hasAlt
    type: bool
    description:
    value: True
  - name: hasShift
    type: bool
    description:
    value: True
  - name: key
    type: number
    description:
    value: 92
---

::note
This trigger replaces the `Hot Keys` configuration found in older versions of Streamer.bot
::
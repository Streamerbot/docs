---
title: Set Microphone Output Volume
description: Set the output volume of a specific microphone
version: 0.2.0
parameters:
  - name: Microphone
    type: Select
    required: true
    description: Microphone you want to affect
  - name: Output Volume
    type: Number
    required: true
    description: Output volume of the microphone. Decimal value 0.0 to 1.0 (inclusive)
    default: 42
  - name: Adjustement
    type: Toggle
    description: Will add/subtract from the current volume instead
    default: false
---
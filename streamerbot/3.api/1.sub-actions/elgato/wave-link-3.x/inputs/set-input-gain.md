---
title: Set Input Gain
description: Sets the gain of a specific audio input device
version: 1.1.0
parameters:
  - name: Input Device
    type: Select
    required: true
    description: Audio input device you want to affect
  - name: Gain
    type: number
    required: true
    description: |
      Gain
      Range: `0` to `1` db
    default: Enabled
---
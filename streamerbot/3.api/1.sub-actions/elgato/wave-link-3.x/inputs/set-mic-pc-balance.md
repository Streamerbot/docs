---
title: Set Mic/PC Balance
description: Sets the balance between the microphone and PC audio input
version: 1.1.0
parameters:
  - name: Input Device
    type: Select
    required: true
    description: Audio input device you want to affect
  - name: Mic/PC Mix
    type: number
    required: true
    description: |
      Mic/PC Mix
      Range: `0` to `100`
    default: 100
---
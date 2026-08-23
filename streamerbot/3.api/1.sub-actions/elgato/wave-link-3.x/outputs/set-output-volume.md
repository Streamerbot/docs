---
title: Set Output Volume
description: Sets the volume of a specific audio output
version: 1.1.0
parameters:
  - name: Output Device
    type: Select
    required: true
    description: Audio output device you want to affect
  - name: Volume
    type: number
    required: true
    description: |
      Gain
      Range: `0` to `100`
    default: 100
---

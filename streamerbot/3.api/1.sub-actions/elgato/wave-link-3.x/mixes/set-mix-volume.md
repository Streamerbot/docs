---
title: Set Mix Volume
description: Sets the volume of a specific audio mix
version: 1.1.0
parameters:
  - name: Mix
    type: Select
    required: true
    description: Audio mix you want to affect
  - name: Volume
    type: number
    required: true
    description: |
      Gain
      Range: `0` to `100` db
    default: 100
---

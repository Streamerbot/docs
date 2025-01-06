---
title: Set Input Volume
description: Set the volume of an audio input
version: 0.2.0
parameters:
  - name: Input
    type: Select
    required: true
    description: Audio input you want to affect
  - name: Mixer
    type: Select
    required: true
    description: Mix you want to affect
  - name: Volume
    type: Number
    required: true
    description: Volume of the audio input mix
    default: 42
  - name: Adjustement
    type: Toggle
    description: Will add/subtract from the current volume instead
    default: false
---

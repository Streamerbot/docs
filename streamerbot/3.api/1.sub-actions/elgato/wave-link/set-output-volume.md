---
title: Set Output Volume
description: Set the output volume of an audio output
version: 0.2.0
parameters:
  - name: Output
    type: Select
    required: true
    description: Audio output you want to affect
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
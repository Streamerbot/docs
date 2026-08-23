---
title: Set Channel Volume
description: Set the output volume of an audio channel
version: 1.1.0
parameters:
  - name: Channel
    type: Select
    required: true
    description: Audio channel you want to affect
  - name: Mix
    type: Select
    required: true
    description: Audio input mix you want to affect
  - name: Volume
    type: Number
    required: true
    description: Volume of the audio input mix
    default: 100
---

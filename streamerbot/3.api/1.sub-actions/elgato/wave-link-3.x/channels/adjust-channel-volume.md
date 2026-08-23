---
title: Adjust Channel Volume
description: Adjust the volume of an audio channel
version: 1.1.0
parameters:
  - name: Channel
    type: Select
    required: true
    description: Audio channel you want to affect
  - name: Mix
    type: Select
    required: true
    description: Desired mix of the channel you want to affect
  - name: Volume Delta
    type: Number
    description: Will add/subtract from the current volume
    default: +5
---

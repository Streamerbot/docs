---
title: Set Channel Mix Mute
description: Mute a specific mix within an audio channel
version: 1.1.0
parameters:
  - name: Channel
    type: Select
    required: true
    description: Audio channel you want to affect
  - name: Mix
    type: Select
    required: true
    description: Mix which should be affected
  - name: State
    type: Select
    required: true
    description: |
      Mute State
      Options: `Muted`, `Not Muted`, `Toggle`
    default: Muted
---
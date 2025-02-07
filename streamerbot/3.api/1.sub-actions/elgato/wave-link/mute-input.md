---
title: Mute Input
description: Mute a specific audio input
version: 0.2.0
parameters:
  - name: Input
    type: Select
    required: true
    description: Audio input you want to affect
  - name: Mixer
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
---
title: Mute Output
description: Mute a specific audio output
version: 0.2.0
parameters:
  - name: Output
    type: Select
    required: true
    description: Audio output you want to affect
  - name: State
    type: Select
    required: true
    description: |
      Mute State
      Options: `Muted`, `Not Muted`, `Toggle`
    default: Muted
---
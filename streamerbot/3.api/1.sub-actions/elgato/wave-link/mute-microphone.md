---
title: Mute Microphone
description: Mute a specific microphone
version: 0.2.0
parameters:
  - name: Microphone
    type: Select
    required: true
    description: Microphone you want to affect
  - name: State
    type: Select
    required: true
    description: |
      Mute State
      Options: `Muted`, `Not Muted`, `Toggle`
    default: Muted
---
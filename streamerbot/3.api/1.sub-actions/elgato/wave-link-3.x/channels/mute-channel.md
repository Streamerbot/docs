---
title: Mute Channel
description: Mute a specific audio channel
version: 1.1.0
parameters:
  - name: Channel
    type: Select
    required: true
    description: Audio channel you want to affect
  - name: State
    type: Select
    required: true
    description: |
      Mute State
      Options: `Muted`, `Not Muted`, `Toggle`
    default: Muted
---
:wip
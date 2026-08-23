---
title: Set Channel Effect State
description: Set the state of a specific effect within an audio channel
version: 1.1.0
parameters:
  - name: Channel
    type: Select
    required: true
    description: Audio channel you want to affect
  - name: Effect
    type: Select
    required: true
    description: Effect which should be applied to the audio channel
  - name: State
    type: Select
    required: true
    description: |
      Effect State
      Options: `Disabled`, `Enabled`, `Toggle`
    default: Disabled
---
:wip
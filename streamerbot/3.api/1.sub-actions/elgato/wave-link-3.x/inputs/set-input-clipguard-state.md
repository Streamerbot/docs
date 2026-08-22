---
title: Set Input Clipguard State
description: Sets the clipguard state of a specific audio input device
version: 1.1.0
parameters:
  - name: Input Device
    type: Select
    required: true
    description: Audio input device you want to affect
  - name: State
    type: Select
    required: true
    description: |
      State
      Options: `Enabled`, `Disabled`, `Toggle`
    default: Enabled
---
:wip
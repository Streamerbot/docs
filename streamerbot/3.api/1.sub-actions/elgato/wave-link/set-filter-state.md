---
title: Set Filter State
description: Change the state of a specific filter of an audio input
version: 0.2.0
parameters:
  - name: Input
    type: Select
    required: true
    description: Audio input you want to affect
  - name: Filter
    type: Select
    required: true
    description: Filter you want to affect
  - name: State
    type: Select
    required: true
    description: Filter State
    default: Enabled / Disabled / Toggle
---
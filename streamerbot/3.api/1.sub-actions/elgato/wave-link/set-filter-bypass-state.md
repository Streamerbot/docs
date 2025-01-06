---
title: Set Filter Bypass State
description: Enable or bypass a filter of an audio input
version: 0.2.0
parameters:
  - name: Input
    type: Select
    required: true
    description: Audio input you want to affect
  - name: Mixer
    type: Select
    required: true
    description: Mix you want to affect
  - name: State
    type: Select
    required: true
    description: Mute state
    default: Bypass / Enabled / Toggle
---
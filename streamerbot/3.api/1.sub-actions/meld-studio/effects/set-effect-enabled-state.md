---
title: Meld Studio Set Effect Enabled State
description: Sets the enabled state of the selected effect in Meld Studio
version: 0.2.5
parameters:
  - name: MeldStudioConnection
  - name: MeldStudioScene
  - name: MeldStudioLayer
  - name: MeldStudioEffect
  - name: State
    type: Select
    required: true
    description: |
      Select which state you want to set

      - `Visible`: Sets the effect state on your scene to Visible
      - `Hidden`: Sets the effect state on your scene to Hidden
      - `Toggle`: Toggles the effect state on your scene between Visible and Hidden
variables: []
---

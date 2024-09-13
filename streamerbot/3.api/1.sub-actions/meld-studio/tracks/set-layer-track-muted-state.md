---
title: Set Layer Track Muted State
description: Mute or unmute a Track associated with a Layer in Meld Studio
version: 0.2.5
parameters:
  - name: MeldStudioConnection
  - name: MeldStudioScene
  - name: MeldStudioLayer
  - name: MeldStudioTrack
  - name: State
    type: Select
    required: true
    description: |
      Select the mute state for the source

      - `Muted`: Set the mute state to muted
      - `Not Muted`: Set the mute state to not muted
      - `Toggle`: Toggle the mute state between muted and not muted
variables: []
---

---
title: Set Source Mute State
description: Mute or unmute a source in Streamlabs Desktop
parameters:
  - name: SlobsConnection
  - name: SlobsScene
  - name: SlobsSource
  - name: State
    type: Select
    required: true
    description: |
      Select the mute status for the source

      - `Muted`: Set the mute state to muted
      - `Not Muted`: Set the mute state to not muted
      - `Toggle`: Toggle the mute state between muted and not muted
variables: []
csharpMethods:
  - SlobsSetSourceMuteState
---

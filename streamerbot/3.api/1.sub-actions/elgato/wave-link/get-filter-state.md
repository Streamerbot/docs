---
title: Get Filter State
description: Get the current state of a specific filter of an input
version: 0.2.0
parameters:
  - name: Input
    type: Select
    required: true
    description: Audio input you want to change the filter of
  - name: Filter
    type: Select
    required: true
    description: Filter you want to get state of
variables:
  - name: input.identifier
    type: string
    description: Identifier of the audio input
    value: ABCD_1234
  - name: input.name
    type: string
    description: Name of the audio input
    value: Microphone
  - name: filter.id
    type: string
    description: Indentifier of the selected filter
    value: 123456-1234-1234-ABCD-ABCDE12345
  - name: filter.name
    type: string
    description: Name of the filter
    value: Elgato Noise Removal
  - name: filter.active
    type: bool
    description: Indicates if filter is enabled
    value: True
  - name: filter.pluginId
    type: string
    description: ID of the filter plugin
    value: e954837c
---

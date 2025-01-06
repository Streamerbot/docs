---
title: Get Input Information
description: Get information of a select audio input
version: 0.2.0
parameters:
  - name: Input
    type: Select
    required: true
    description: Audio input you want to get information about
variables:
  - name: input.identifier
    type: string
    description: Identifier of the audio input
    value: PCM_OUT_01_V_02_SD3
  - name: input.name
    type: string
    description: Name of the audio input
    value: Music
  - name: input.local.muted
    type: bool
    description: Indicator whether your own mix is muted
    value: False
  - name: input.local.volume
    type: int
    description: Volume level of your own mix
    value: 100
  - name: input.local.filterBypass
    type: bool
    description: Indicates if filters are bypassed in your own mix
    value: False
  - name: input.stream.muted
    type: bool
    description: Indicator whether the stream mix is muted
    value: False
  - name: input.stream.volume
    type: int
    description: Volume level of the stream mix
    value: 42
  - name: input.stream.filterBypass
    type: bool
    description: Indicates if filters are bypassed in the stream mix
    value: False
---

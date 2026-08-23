---
title: Get Mix Information
description: Retrieve information about an audio mix
version: 1.1.0
parameters:
  - name: Mix
    type: Select
    required: true
    description: Audio mix you want to obtain the current information for
variables:
  - name: waveLinkMixId
    type: string
    description: Identifier of the mix ID
    value: PCM_IN_01_V_04_SD3
  - name: waveLinkMixName
    type: string
    description: Name of the mix
    value: Chat Mix
  - name: waveLinkMixVolume
    type: number
    description: Current volume level of the mix
    value: 1
  - name: waveLinkMixMuted
    type: bool
    description: Indicates if the mix is muted
    value: false
---

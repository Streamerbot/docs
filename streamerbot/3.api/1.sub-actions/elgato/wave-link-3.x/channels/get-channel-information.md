---
title: Get Channel Information
description: Retrieve information about an audio channel
version: 1.1.0
parameters:
  - name: Channel
    type: Select
    required: true
    description: Audio channel you want to obtain the current information for
variables:
  - name: waveLinkChannelId
    type: string
    description: Identifier of the channel ID
    value: PCM_OUT_00_V_00_SD1
  - name: waveLinkChannelName
    type: string
    description: Name of the channel
    value: System
  - name: waveLinkChannelVolume
    type: number
    description: Current volume level of the channel
    value: 1
  - name: waveLinkChannelMuted
    type: bool
    description: Indicates if the channel is muted
    value: false
  - name: waveLinkChannelLevel
    type: number
    description: Current volume level of the channel
    value: 1
  - name: waveLinkChannelEffectsCount
    type: number
    description: Current number of effects applied to the channel
    value: 0
  - name: waveLinkChannelMixesCount
    type: number
    description: Current number of mixes the channel is part of
    value: 2
  - name: waveLinkChannelMix.0.id
    type: string
    description: ID of the first mix the channel is part of
    value: PCM_IN_01_V_00_SD1
  - name: waveLinkChannelMix.0.name
    type: string
    description: Name of the first mix the channel is part of
    value: Testing Name Mix
  - name: waveLinkChannelMix.0.level
    type: number
    description: Volume level of the first mix the channel is part of
    value: 1
  - name: waveLinkChannelMix.0.muted
    type: bool
    description: Indicates if the first mix the channel is part of is muted
    value: false
  - name: waveLinkChannelMix.1.id
    type: string
    description: ID of the second mix the channel is part of
    value: PCM_IN_01_V_02_SD2
  - name: waveLinkChannelMix.1.name
    type: string
    description: Name of the second mix the channel is part of
    value: Stream Mix
  - name: waveLinkChannelMix.1.level
    type: number
    description: Volume level of the second mix the channel is part of
    value: 1
  - name: waveLinkChannelMix.1.muted
    type: bool
    description: Indicates if the second mix the channel is part of is muted
    value: false
---

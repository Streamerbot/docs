---
title: Get Input Device Information
description: Retrieve information about an audio input device
version: 1.1.0
parameters:
  - name: Input Device
    type: Select
    required: true
    description: Audio input device you want to obtain the current information for
variables:
  - name: waveLinkInputDeviceId
    type: string
    description: Identifier of the input device
    value: '{0.0.1.00000000}.{96e65e84-0aaf-4b18-8f69-3da2d478b3d4}'
  - name: waveLinkInputDeviceName
    type: string
    description: Name of the input device
    value: Microphone (2- Realtek USB2.0 Audio)
  - name: waveLinkInputDeviceType
    type: string
    description: Type of the input device
    value: thirdParty
  - name: waveLinkInputDeviceGain
    type: number
    description: Current gain level of the input device
    value: 0.5541552
  - name: waveLinkInputDeviceMuted
    type: bool
    description: Indicates if the input device is muted
    value: false
  - name: waveLinkInputDeviceMicPcMix
    type: number
    description: Current microphone/PC mix level of the input device
    value: 0
  - name: waveLinkInputDeviceClipGuard
    type: bool
    description: Indicates if the input device has clip guard enabled
    value: false
  - name: waveLinkInputDeviceLowCutFilter
    type: bool
    description: Indicates if the input device has low cut filter enabled
    value: false
  - name: waveLinkInputDeviceChannelCount
    type: number
    description: Number of channels of the input device
    value: 0
  - name: waveLinkInputChannelId
    type: string
    description: Identifier of the input channel
    value:   
  - name: waveLinkInputChannelName
    type: string
    description: Name of the input channel
    value:   
  - name: waveLinkInputChannelVolume
    type: number
    description: Current volume level of the channel
    value: 0
  - name: waveLinkInputChannelMuted
    type: bool
    description: Indicates if the input channel is muted
    value: false
---
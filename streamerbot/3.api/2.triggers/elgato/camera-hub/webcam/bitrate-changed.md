---
title: Bitrate Changed
description: When the selected `Bitrate` changed for EpocCam
variables:
  - name: bitrate
    type: string
    description: The name of the `Bitrate` that was selected
    value: Medium
  - name: bitrateIndex
    type: number
    description: The zero based index of the `Bitrate` that was selected
    value: 1
  - name: oldBitrate
    type: string
    description: The name of the `Bitrate` that was previously selected
    value: Lowest
  - name: oldBitrateIndex
    type: number
    description: The zero based index of the `Bitrate` that was previously selected
    value: 0
  - name: success
    type: boolean
    description: Returns whether or not the bitrate was sucessfully changed
    value: True    
support:
  - name: epoccam
---

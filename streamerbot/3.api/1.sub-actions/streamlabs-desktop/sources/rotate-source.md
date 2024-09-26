---
title: Hide Source's Filters
description: Hide all filters from a given source
parameters:
  - name: SlobsConnection
  - name: SlobsScene
  - name: SlobsSource
  - name: Alignment
    description: |
      Shows the current alignment
  - name: Rotation
    type: Number
    default: 0
    description: |
      By default, this is an `Absolute` angle with 0 being normal rotation, valid range `-360`{lang=cs} to `+360`{lang=cs},

      Negative values will rotate the source counter-clockwise.
  - name: Additive
    type: Toggle
    default: false
    description: |
      This option will make the rotation relative to its current alignment, rather than overwriting
variables: []
csharpMethods: []
---

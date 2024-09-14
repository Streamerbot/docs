---
title: Rotate Source
description: Rotate a source
parameters:
  - name: ObsConnection
    type: Select
    required: true
    description: |
      Select the Connection from the drop-down
      - Any, Default, or named connections will appear here
  - name: ObsScene
    type: Select
    required: true
    description: |
      Select a Scene from the drop-down
      - Can also manually type the Scene name into the box
  - name: ObsSource
    type: Select
    required: true
    description: |
      Select a Source from the drop-down
      - Can also manually type the Source name into the box
  - name: Alignment
    type: Select
    required: true
    description: |
      This shows the current alignment of the source

      - This field is not editable
  - name: Rotation
    type: Number
    required: true
    description: |
      By default, this is an `Absolute` angle with 0 being normal rotation, valid range -360 -> +360, however as transform is instant values outside -180 -> +180 will be visually the same. Negative values rotate the source counter-clockwise.
  - name: Additive
    type: Checkbox
    required: true
    description: |
      This option will make the rotation relative to its current transform rather than overwriting
variables: []
csharpMethods: []
---
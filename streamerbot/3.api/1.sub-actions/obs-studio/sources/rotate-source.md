---
title: Rotate Source
description: Rotate a source
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
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
---
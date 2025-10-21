---
title: Flip Source
description: Flip a source horizontally, vertically or both
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
  - name: Mode
    type: Select
    required: true
    description: Select the direction to flip the source
    default: Horizontal
    options:
      - value: Horizontal
        description: Flip the source horizontally
      - value: Vertical
        description: Flip the source vertically
      - value: Both
        description: Flip the source both horizontally and vertically
variables: []
csharpMethods: []
---
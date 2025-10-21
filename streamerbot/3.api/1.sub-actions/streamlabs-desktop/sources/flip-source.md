---
title: Flip Source
description: Flip a source horizontally, vertically, or both
parameters:
  - name: Connection
    import: streamlabs-desktop/connection
  - name: Scene
    import: streamlabs-desktop/scene
  - name: Source
    import: streamlabs-desktop/source
  - name: Mode
    type: Select
    required: true
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
---
title: Set Media State
description: Set the status of the media source
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
  - name: State
    type: Select
    required: true
    description: Select the playback state for the selected Media
    options:
      - value: Play
        description: Play your Media Source
      - value: Pause
        description: Pause your Media Source
      - value: Restart
        description: Restart your Media Source
      - value: Stop
        description: Stop your Media Source
      - value: Next
        description: Go next on your Media Source
      - value: Previous
        description: Go to the previous on your Media Source
variables: []
csharpMethods:
  - ObsSetMediaState
---
---
title: Recording
description: Change your Meld Studio recording status
version: 0.2.5
parameters:
  - name: Connection
    import: meld-studio/connection
  - name: State
    type: Select
    required: true
    description: Choose the recording state
    options:
      - value: Start
        description: Start your recording status
      - value: Stop
        description: Stop your recording status
      - value: Toggle
        description: Toggle your recording status
variables: []
---

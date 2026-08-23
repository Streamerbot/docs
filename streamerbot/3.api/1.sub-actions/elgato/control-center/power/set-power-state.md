---
title: Set Power State
description: Set the power state of the selected device in Elgato Control Center
version: 1.1.0
parameters:
  - name: Device
    type: Select
    required: true
    description: Device to set the power state for
  - name: State
    type: Select
    required: true
    description: Power state for the device
    options:
      - Off
      - On
      - Toggle
---
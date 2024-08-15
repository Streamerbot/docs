---
title: Webcam Set Zoom
description: Sets the desired zoom
version: 0.2.3
parameters:
  - name: Zoom
    type: Int
    required: true
    description: Enter percentage (100-400) in the input box
  - name: Adjustment
    type: Checkbox
    required: False
    description: If checked, the amount entered in the 'Zoom' box will be added to the current setting
support:
  - name: facecam
    partial: true
    description: Zoom is supported in increments of 10
  - name: facecam-mk2
  - name: facecam-pro
---

:wip

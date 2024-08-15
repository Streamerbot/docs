---
title: Webcam Set Sharpness
description: Sets the desired sharpness
version: 0.2.3
parameters:
  - name: Sharpness
    type: Int
    required: true
    description: Enter (0-4) in the input box
  - name: Adjustment
    type: Checkbox
    required: False
    description: If checked, the amount entered in the 'Sharpness' box will be added to the current setting
support:
  - name: facecam
    partial: true
    description: Sharpness is supported as values of 0 to 4
  - name: facecam-mk2
  - name: facecam-pro
---

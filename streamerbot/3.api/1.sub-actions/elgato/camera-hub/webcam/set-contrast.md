---
title: Webcam Set Contrast
description: Sets the desired contrast
version: 0.2.3
parameters:
  - name: Contrast
    type: Int
    required: true
    description: Enter percentage (0-100) in the input box
  - name: Adjustment
    type: Checkbox
    required: False
    description: If checked, the amount entered in the 'Contrast' box will be added to the current setting
support:
  - name: facecam
    partial: true
    description: Contrast is supported, but in increments of 10%
  - name: facecam-mk2
  - name: facecam-pro
---

---
title: Activate Lens
description: Activatres the selected Lens in StreamFog
version: 1.0.5
parameters:
  - name: Category
    type: Select
    required: true
    description: Select the category for the desired lens
    options:
      - value: Art Styles
      - value: Beauty
      - value: Bodywear & Costumes
      - value: Face Filters
      - value: Face Masks
      - value: Hair & Beard
      - value: Headwear
      - value: Visual Effects
      - value: VTube
  - name: Lens
    type: Select
    required: true
    description: Select the desired lens to activate
  - name: Duration
    type: Number
    description: Optional duration to activate the Lens for (if left blank, the Lens will be activated indefinitely until deactivated)
---

---
title: Color Tint
description: Tint ArtMeshes by providing a color and matching criteria
parameters:
  - name: Color
    type: String
    required: true
    description: Color hex code
  - name: Mix With Scene Lighting Color
    type: Double
    required: false
    description: Determines how the tint color is mixed with the scene lighting system color (between 0 and 1)
  - name: Random Color
    type: Checkbox
    required: false
    description: Assigns a random color
  - name: Tint All
    type: Checkbox
    required: false
    description: Tints the entire model
  - name: Filter Type
    type: Selection
    required: false
    description: Allows to filter for art mesh number, tags or names
  - name: Values
    type: Input
    required: false
    description: Assign a filter value, like `D_TAIL_03` for the exact name of the model's tail.
variables: []
csharpMethods:
  - VTubeStudioColorTintAll
  - VTubeStudioColorTintByNameContains
  - VTubeStudioColorTintByNames
  - VTubeStudioColorTintByNumber
  - VTubeStudioColorTintByTagContains
  - VTubeStudioColorTintByTags
---

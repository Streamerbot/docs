---
title: Take Screenshot
description: Makes a screenshot from a scene or source
parameters:
  - name: ObsConnection
    type: Select
    required: true
    description: |
      Select the Connection from the drop-down
      - Any, Default, or named connections will appear here
  - name: ObsScene
    type: Select
    required: true
    description: |
      Select a Scene from the drop-down
      - Can also manually type the Scene name into the box
  - name: ObsSource
    type: Select
    required: true
    description: |
      Select a Source from the drop-down
      - Can also manually type the Source name into the box
  - name: File Path
    type: String
    required: true
    description: |
      Select the file path for the screenshot
  - name: Quality
    type: Slider
    required: true
    description: |
      Select the image quality or leave as `Auto`  
variables:
  - name: screenshotFile
    type: string
    description: The full path to the screenshot that was taken
  - name: filedatetime
    type: DateTime
    description: Date Time variable that can be used for file name `yyyyMMdd.hhmmss`
    value: 8/4/2023 10:56:06 AM
csharpMethods:
  - ObsTakeScreenshot
---
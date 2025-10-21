---
title: Take Screenshot
description: Create a screenshot from a selected scene or source
parameters:
- name: Connection
  import: obs-studio/connection
- name: Scene
  import: obs-studio/scene
- name: Source
  import: obs-studio/source
- name: File Path
  required: true
  type: String
  description: |
    Select the file path for the screenshot

    ::note
    When using the `Test` Button in the dialog, arguments will **NOT** be populated.
    This only tests the literal string entered into the input.
    ::
- name: Quality
  description: Select the image quality for the generated sreenshot
  required: true
  type: Slider
  default: Auto
variables:
  - description: The full path to the screenshot that was taken
    name: screenshotFile
    type: string
  - description: Date Time variable that can be used for file name `yyyyMMdd.hhmmss`
    name: filedatetime
    type: DateTime
    value: 8/4/2023 10:56:06 AM
csharpMethods:
  - ObsTakeScreenshot
---

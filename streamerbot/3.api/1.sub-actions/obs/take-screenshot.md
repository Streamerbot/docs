---
title: Take Screenshot
description: Makes a screenshot from a scene or source
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

## Parameters
::field-group
  :parameter{name=ObsConnection}
  :parameter{name=ObsScene}
  :parameter{name=ObsSource}
  ::field{name="File Path" type=File required}
    Select the file path for the screenshot
  ::
  ::field{name="Quality" type=Slider required}
    Select the image quality or leave as `Auto`
  ::
::
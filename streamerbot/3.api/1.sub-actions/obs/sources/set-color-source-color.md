---
title: Set Color Source Color
description: Set a random or a HEX color for a color source
variables: []
csharpMethods:
  - ObsSetColorSourceColor
  - ObsSetColorSourceRandomColor
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
  :parameter{name=ObsScene}
  :parameter{name=ObsSource}
  ::field{name="Random Color" type=Checkbox}
    This gets a random HEX color each time this sub-action runs
  ::
  ::field{name=Color type=Color required}
    Choose a color, using the `#RRGGBBAA` format
  ::
::

---
title: Rotate Source
description: Rotate a source
variables: []
csharpMethods: []
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
  :parameter{name=ObsScene}
  :parameter{name=ObsSource}
  ::field{name=Alignment type=Select}
    This shows the current alignment of the source

    - This field is not editable
  ::
  ::field{name=Rotation type=Number required}
    By default, this is an `Absolute` angle with 0 being normal rotation, valid range -360 -> +360, however as transform is instant values outside -180 -> +180 will be visually the same. Negative values rotate the source counter-clockwise.
  ::
  ::field{name=Additive type=Number required}
    This option will make the rotation relative to its current transform rather than overwriting
  ::
::
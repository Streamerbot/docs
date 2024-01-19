---
title: Delay
description: Add a delay between sub-actions
variables: []
csharpMethods:
  - Wait
---

:image-preview

## Parameters
::field-group
  ::field{name=Delay type=Number required}
    The duration of the delay
  ::

  ::field{name=Random type=Checkbox}
    Generate a random delay between min/max values
  ::

  ::field{name=To type=Checkbox}
    If `Random` is selected, a random delay will be selected between the `Delay` and `To` values
  ::
::
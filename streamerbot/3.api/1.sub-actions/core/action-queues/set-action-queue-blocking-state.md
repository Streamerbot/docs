---
title: Set Action Queue Blocking State
description: Toggle blocking on or off for an Action Queue
variables: []
---

## Parameters
::field-group
  ::field{name=Queue type=Select required}
  Select an existing action queue
  ::

  ::field{name=State type=Select default=Enabled required}
  - `Enabled` - Enable the blocking state for the selected queue
  - `Disabled` - Disable the blocking state for the selected queue
  - `Toggle` - Toggle the existing blocking state
  ::
::
---
title: Set Action Queue Pause State
description: Pause or resume an Action Queue
variables: []
---

::tip
Pausing all queues will effectively disable the bot from performing any commands, alerts, redeems, etc., until the queue is resumed.
::

## Parameters
::field-group
  ::field{name=Queue type=Select required}
  Select an existing action queue to, or select `All` to modify all queues
  ::

  ::field{name=State type=Select default=Pause required}
  - `Pause` - Pause the selected queue
  - `Resume` - Resume the selected queue
  ::

  ::field{name=Clear type=Toggle default="false"}
    Also remove all pending actions in the queue
  ::
::
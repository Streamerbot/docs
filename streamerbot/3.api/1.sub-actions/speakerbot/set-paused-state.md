---
title: Set Paused State
description: Toggle the state of the Speaker.bot TTS queue
version: 0.2.3
variables: []
---

:read-more{to=/guide/integrations/speakerbot}

## Parameters
::field-group
  ::field{name=State type=Select required default="Paused"}
  - `Paused`: Pause the TTS queue
  - `Enabled`: Resume the TTS queue
  - `Toggle`: Toggle the existing state
  ::
::
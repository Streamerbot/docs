---
name: ObsSetRandomFilterState
title: ObsSetRandomFilterState
description: Set the state of a random OBS filter within a scene and/or source<br>State => 0 = enable, 1 = disable, 2 = toggle
parameters:
  - import: ObsScene
  - import: ObsSource
  - import: ObsFilterName
  - import: ObsFilterState
  - import: ObsConnection
---
---
title: Set State of a Random Filter
description: Set the state of a filter randomly selected from a given scene or source
csharpMethods:
  - SlobsSetRandomSceneFilterState
  - SlobsSetRandomSourceFilterState
---

## Parameters
:parameter{name=SlobsConnection}

### `Scene`
Select the scene from this dropdown list, you can also manually enter a scene name.

- Type: `String`

### `Source`
Select the source from this dropdown list, you can also manually enter a source name.

- Type: `String`

### `State`
Set the state for the random filter

- `Visible`: Set the filter state to visible
- `Hidden`: Set the filter state to hidden
- `Toggle`: Toggle the filter state between visible and hidden
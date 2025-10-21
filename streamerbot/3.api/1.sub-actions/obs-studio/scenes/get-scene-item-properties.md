---
title: Get Scene Item Properties
description: Get the source properties of a scene item
variables:
  - name: props.bounds.alignment
    type: string
    description: The alignment of the bounding box
  - name: props.bounds.type
    type: string
    description: The type of bounding box
    value: OBS_BOUNDS_STRETCH, OBS_BOUNDS_SCALE_INNER, OBS_BOUNDS_SCALE_OUTER, OBS_BOUNDS_SCALE_TO_WIDTH, OBS_BOUNDS_SCALE_TO_HEIGHT, OBS_BOUNDS_MAX_ONLY or OBS_BOUNDS_NONE
  - name: props.bounds.x
    type: number
    description: The width of the bounding box
  - name: props.bounds.y
    type: number
    description: The height of the bounding box
  - name: props.crop.bottom
    type: number
    description: The number of pixels cropped off the bottom of the source before scaling
  - name: props.crop.left
    type: number
    description: The number of pixels cropped off the left of the source before scaling
  - name: props.crop.right
    type: number
    description: The number of pixels cropped off the right of the source before scaling
  - name: props.crop.top
    type: number
    description: The number of pixels cropped off the top of the source before scaling
  - name: props.height
    type: number
    description: Scene item height (base source height multiplied by the vertical scaling factor)
  - name: props.itemId
    type: string
    description: The scene Item id
  - name: props.locked
    type: boolean
    description: If the source's transform is locked
    value: True
  - name: props.message-id
    type: string
    description: The id of the message
  - name: props.muted
    type: boolean
    description: If the source is muted
    value: True
  - name: props.name
    type: string
    description: Scene Item name
  - name: props.position.alignment
    type: string
    description: The point on the source that the item is manipulated from. The sum of 1=Left or 2=Right, and 4=Top or 8=Bottom, or omit to centre on that axis
  - name: props.position.x
    type: number
    description: The x position of the source from the left
  - name: props.position.y
    type: number
    description: The y position of the source from the top
  - name: props.rotation
    type: number
    description: The clockwise rotation of the item in degrees around the point of alignment
  - name: props.scale.filter
    type: string
    description: The scale filter of the source
    value: OBS_SCALE_DISABLE, OBS_SCALE_POINT, OBS_SCALE_BICUBIC, OBS_SCALE_BILINEAR, OBS_SCALE_LANCZOS or OBS_SCALE_AREA
  - name: props.scale.x
    type: number
    description: The x-scale factor of the source
  - name: props.scale.y
    type: number
    description: The y-scale factor of the source
  - name: props.sourceHeight
    type: number
    description: Base source (without scaling) of the source
  - name: props.sourceWidth
    type: number
    description: Base width (without scaling) of the source
  - name: props.status
    type: string
    description: The status of the sub-action
  - name: props.visible
    type: boolean
    description: If the source is visible
    value: True
  - name: props.width
    type: number
    description: Scene item width (base source width multiplied by the horizontal scaling factor)
  - name: props.groupChildren[#].<one of these above>
    type: any
    description: List of children (if this item is a group)
  - name: props._json
    type: string
    description: Everything above in a json format
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
csharpMethods:
  - ObsGetSceneItemProperties
---
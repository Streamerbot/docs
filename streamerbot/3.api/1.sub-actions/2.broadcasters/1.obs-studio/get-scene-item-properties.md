# Get Scene Item Properties
Get the source properties of a scene item
:image-preview

## Parameters
:parameter{name=ObsConnection}

### `Scene`
Select the scene from this dropdown list, you can also manually enter a scene name.

- Type: `String`

### `Source`
Select the source from this dropdown list, you can also manually enter a source name.

- Type: `String`

## Variables
Name | Description
----:|:------------
`props.bounds.alignment` | Alignment of the bounding box
`props.bounds.type` | Type of bounding box, Can be `OBS_BOUNDS_STRETCH`, `OBS_BOUNDS_SCALE_INNER`, `OBS_BOUNDS_SCALE_OUTER`, `OBS_BOUNDS_SCALE_TO_WIDTH`, `OBS_BOUNDS_SCALE_TO_HEIGHT`, `OBS_BOUNDS_MAX_ONLY` or `OBS_BOUNDS_NONE`.
`props.bounds.x` | Width of the bounding box
`props.bounds.y` | Height of the bounding box
`props.crop.bottom` | The number of pixels cropped off the bottom of the source before scaling
`props.crop.left` | The number of pixels cropped off the left of the source before scaling
`props.crop.right` | The number of pixels cropped off the right of the source before scaling
`props.crop.top` | The number of pixels cropped off the top of the source before scaling
`props.height` | Scene item height (base source height multiplied by the vertical scaling factor)
`props.itemId` | Scene Item ID
`props.locked` | If the source's transform is locked
`props.message-id` | The id of the message
`props.muted` | If the source is muted
`props.name` | Scene Item name
`props.position.alignment` | The point on the source that the item is manipulated from. The sum of 1=Left or 2=Right, and 4=Top or 8=Bottom, or omit to centre on that axis
`props.position.x` | The x position of the source from the left
`props.position.y` | The y position of the source from the top
`props.rotation` | The clockwise rotation of the item in degrees around the point of alignment
`props.scale.filter` | The scale filter of the source. Can be `OBS_SCALE_DISABLE`, `OBS_SCALE_POINT`, `OBS_SCALE_BICUBIC`, `OBS_SCALE_BILINEAR`, `OBS_SCALE_LANCZOS` or `OBS_SCALE_AREA`
`props.scale.x` | The x-scale factor of the source
`props.scale.y` | The y-scale factor of the source
`props.sourceHeight` | Base source (without scaling) of the source
`props.sourceWidth` | Base width (without scaling) of the source
`props.status` | The status of the sub-action
`props.visible` | If the source is visible
`props.width` | Scene item width (base source width multiplied by the horizontal scaling factor)
`props.groupChildren[#].<one of these above>` | List of children (if this item is a group)
`props._json` | Everything above in a json format

## C# Usage
:csharp-method{name=ObsGetSceneItemProperties}
# Rotate Source
Rotate a source
:image-preview

## Parameters
:parameter{name=SlobsConnection}

### `Scene`
Select the scene from this dropdown list, you can also manually enter a scene name.

- Type: `String`

### `Source`
Select the source from this dropdown list, you can also manually enter a source name.

- Type: `String`

### `Alignment`
This shows the current alignment.

### `Rotation`
By default this is an `Absolute` angle with 0 being normal rotation, valid range -360 -> +360, however as tranform is instant values outside -180 -> +180 will be visually the same. Negative values rotate the source counter-clockwise.

- Type: `Number`

### `Additive`
This option will make the rotation relative to its current transform rather than overwriting

## C# Usage
:csharp-method
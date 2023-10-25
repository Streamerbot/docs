# Set Color Source Color
Set a random or a HEX color for a color source
:image-preview

## Parameters
:parameter{name=ObsConnection}

### `Scene`
Select the scene from this dropdown list, you can also manually enter a scene name.

- Type: `String`

### `Source`
Select the source from this dropdown list, you can also manually enter a source name.

- Type: `String`

### `Random Color`
This get a random HEX color each time this sub-action runs.

- Type: `Checkbox`

### `Color`
Choose a color, `#RRGGBBAA` is also supported.

- Type: `Color`

### `Pick Random`
Click this to pick a random color.

## C# Usage
:csharp-method{name=ObsSetColorSourceArgbColor}
:csharp-method{name=ObsSetColorSourceHexColor}
:csharp-method{name=ObsSetColorSourceRandomColor}
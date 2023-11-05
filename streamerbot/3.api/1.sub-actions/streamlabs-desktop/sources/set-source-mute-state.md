# Set Source Mute State
Mute or unmute a source
:image-preview

## Parameters
:parameter{name=SlobsConnection}

### `Scene`
Select the scene from this dropdown list, you can also manually enter a scene name.

- Type: `String`

### `Source`
Select the source from this dropdown list, you can also manually enter a source name.

- Type: `String`

### `State`
Select the mute status for the source

- `Muted`: Set the mute state to muted
- `Not Muted`: Set the mute state to not muted
- `Toggle`: Toggle the mute state between muted and not muted

## C# Usage
:csharp-method{name=SlobsSetSourceMuteState}
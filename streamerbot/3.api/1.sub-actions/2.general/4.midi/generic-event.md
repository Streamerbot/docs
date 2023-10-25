# Generic Event
Send a [Generic MIDI message](https://www.midi.org/specifications-old/item/table-1-summary-of-midi-message) to your MIDI device
:image-preview

## Parameters
### `Name`
Enter a name for this MIDI event

### `Device`
Select a configured MIDI device to send the message to

### `Command`
Select the MIDI event type:

- `NoteOn`
- `NoteOff`
- `ControlChange`
- `PatchChange`
- `ChannelAfterTouch`
- `PitchWheelChange`

### `Channel`
Select a MIDI channel
::list
- *Optional* - Leave blank to broadcast to all channels
::

### `Data1`
Enter a custom value for `Data1` (MIDI Byte 2), or use the `Learn From` option to auto-fill values from your device

### `Data2`
Enter a custom value for `Data2` (MIDI Byte 3), or use the `Learn From` option to auto-fill values from your device

### `Ignore NoteOff`
Ignore `NoteOff` events, useful for devices which send both `NoteOn` and `NoteOff` simultaneously

## C# Usage
:csharp-method
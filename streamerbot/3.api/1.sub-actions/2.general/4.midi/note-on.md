# Note On
Send a [MIDI Note On](https://www.midi.org/specifications-old/item/table-1-summary-of-midi-message) message with Streamer.bot
:image-preview

## Parameters
### `Name`
Enter a name for this MIDI event

### `Device`
Select a configured MIDI device to send the message to

### `Channel`
Select a MIDI channel
::list
- *Optional* - Leave blank to broadcast to all channels
::

### `Note`
Enter a custom value for the `Note Type` (MIDI Byte 2), or use the `Learn From` option to auto-fill values from your device

### `Veolcity`
Enter a custom note `Velocity` (MIDI Byte 3), or use the `Learn From` option to auto-fill values from your device

### `Duration`
Enter a hold duration, in milliseconds

### `Send Note Off`
Toggle to send a `NoteOff` message at the end of the configured [duration](#duration)

## C# Usage
:csharp-method
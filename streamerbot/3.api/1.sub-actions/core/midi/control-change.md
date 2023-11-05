# Control Change
Send a [MIDI Control Change](https://www.midi.org/specifications-old/item/table-3-control-change-messages-data-bytes-2) message with Streamer.bot
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

### `Controller`
Enter a custom value for the `Control Function` (MIDI Byte 2), or use the `Learn From` option to auto-fill values from your device

### `Value`
Enter a custom `Value` (MIDI Byte 3), or use the `Learn From` option to auto-fill values from your device

## C# Usage
:csharp-method
---
title: Control Change
description: Send a MIDI Control Change message with Streamer.bot
---

::read-more{to="https://midi.org/midi-1-0-control-change-messages"}
Read more about MIDI messages at **midi.org**
::

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
Enter a custom value for the `Control Function` (MIDI Byte 2), or use the `Learn From` option to autofill values from your device

### `Value`
Enter a custom `Value` (MIDI Byte 3), or use the `Learn From` option to autofill values from your device

## C# Usage
:csharp-method
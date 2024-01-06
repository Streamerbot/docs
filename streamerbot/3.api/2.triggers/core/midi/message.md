---
title: MIDI Message
description: Trigger for incoming MIDI events
version: 0.1.15
variables:
  - name: name
    type: string
    description: The user-configured `Name` for this device connection
    value: My MPK mini
  - name: deviceName
    type: string
    description: The detected device name
    value: MPKmini2
  - name: timestamp
    type: int
    description: The MIDI timestamp for this message
    value: 1132545
  - name: commandCode
    type: string
    description: The MIDI command type for this message
    value: NoteOn
  - name: commandCodeNum
    type: int
    description: The MIDI command value for this message
    value: 144
  - name: channel
    type: int
    description: The MIDI channel used for this message
    value: 11
  - name: rawMessage
    type: string
    description: The full raw MIDI command value for this message
    value: 00373090
  - name: noteName
    type: string
    description: The note name for this message
    value: C4
  - name: noteNumber
    type: int
    description: The note number for this message
    value: 48
  - name: velocity
    type: int
    description: The velocity value for this message
    value: 80
  - name: velocityNormal
    type: float
    description: The normalized velocity value for this message
    value: 0.62992125984252
  - name: controllerName
    type: string
    description: The MIDI Control Function for this message
    value: Pan
  - name: controllerNumber
    type: int
    description: The MIDI Control Number for this message
    value: 10
  - name: value
    type: int
    description: The value for this message
    value: 80
  - name: valueNormal
    type: float
    description: The normalized value for this message
    value: 0.6299215984252
---

::callout{icon=i-mdi-bookmark to=/guide/midi}
Check out the [MIDI Configuration Guide](#) for details on configuring your MIDI devices
::

:image-preview

## Parameters
::field-group
  ::field{name=Device type=Select required}
    Select a configured MIDI device connection
    - Select `Any` to trigger on **any device**
  ::
  ::field{name=Event type=Select required}
    Select a configured MIDI input event
    - Select `Any` to trigger on **any event**

    ::callout{icon=i-mdi-lightbulb color=amber}
    You can quickly register new [MIDI event listeners](/guide/midi#configuration-1) by clicking the `Add New Event` button!
    ::
  ::
::
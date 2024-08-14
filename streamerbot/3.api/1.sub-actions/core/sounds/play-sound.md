---
title: Play Sound
description: Play an audio file from your computer
parameters:
  - name: Audio Device
    type: Select
    required: true
    default: Application Default
    description: |
      Select an audio device to use for output

      `Application Default` will use the device configured in the Settings tab in Streamer.bot
  - name: Sound file to play
    type: File
    required: true
    description: |
      Select the audio file for playback.

      _Click `...` to open a file browser._

      Supported formats: `mp3`, `wav`, `m4a`, `ogg`
  - name: Finish playing before continuing
    type: Toggle
    default: true
    description: |
      Wait for playback to complete before continuing to the next sub-action.

      When disabled, the sound will play immediately and the next sub-action will begin to execute with no delay.
  - name: Volume
    type: Range
    default: 100
    description: |
      Adjust the output volume

      _This is a simple volume control. It can often be useful to instead adjust the volume with a tool like Audacity._
  - name: Sound Name
    type: string
    descrpition: The name of the sound, this is used in the Stop Sound Playback sub-action
    version: 0.2.4
  - name: Use Filename As Name
    type: boolean
    description: Enabling this will use the filename of the sound as the sound name
    version: 0.2.4
variables: []
csharpMethods:
  - PlaySound
---

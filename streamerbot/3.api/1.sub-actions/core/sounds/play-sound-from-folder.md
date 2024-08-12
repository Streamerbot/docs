---
title: Play Sound From Folder
description: Play a random audio file from a folder
parameters:
  - name: Audio Device
    type: Select
    required: true
    default: Application Default
    description: |
      Select an audio device to use for output

      `Application Default` will use the device configured in the Settings tab in Streamer.bot
  - name: Folder containing...
    type: Folder
    required: true
    description: |
      Select the folder containing the audio files for playback.

      _Click `...` to open a file browser._

      Supported formats: `mp3`, `wav`
  - name: Finish playing before continuing
    type: Toggle
    default: true
    description: |
      Wait for playback to complete before continuing to the next sub-action.

      When disabled, the sound will play immediately and the next sub-action will begin to execute with no delay.
  - name: Recursive
    type: Toggle
    default: false
    description: Include all subdirectories within the selected folder
  - name: Volume
    type: Range
    default: 100
    description: |
      Adjust the output volume

      _This is a simple volume control. It can often be useful to instead adjust the volume with a tool like Audacity._
variables:
  - name: randomSoundFile
    type: string
    description: Full path of the audio file that was randomly selected for playback
    value: 'C:\ScaryNoises\chad.mp3'
  - name: randomSoundFileName
    type: string
    description: File name of the audio file that was randomly selected for playback
    value: 'chad.mp3'
---

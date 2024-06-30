---
title: Play Sound
description: Play a sound of one of your soundboards
version: 0.1.11
parameters:
  - name: Soundboard
    type: Selection
    required: true
    description: Select a soundboard
  - name: Sound
    type: Selection
    required: true
    description: Select a sound
variables: []
csharpMethods: []
---

::warning
VoiceMod starts with an empty default soundboard that is called "My Soundboard". Before you add the subaction, make sure the soundboard has at least one sound assigned to it. Streamer.bot might crash otherwise.
![VoiceMod My Soundboard](assets/voice-soundboard-add.png)
::

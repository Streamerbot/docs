---
title: Select Random Voice
description: Enable a random voice in VoiceMod via Streamer.bot
version: 0.1.8
parameters:
  - name: Mode
    type: Select
    description: Select the mode for choosing a random voice
    required: true
    options:
      - value: All Voices
        description: Select a random voice from all available voices
      - value: Free Voices
        description: Select a random voice from free voices only
      - value: Favourite Voices
        description: Select a random voice from your favourited voices
      - value: Custom Voices
        description: Select a random voice from a custom list of voices
csharpMethopds:
  - VoiceModSelectVoice
---

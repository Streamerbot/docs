---
title: Set Censor State
description: Modify the current censorship state in VoiceMod via Streamer.bot
version: 0.1.8
parameters:
  - name: State
    type: Select
    description: Select the new censorship state to set in VoiceMod
    required: true
    options:
      - value: Enabled
        description: Enable the censor in VoiceMod
      - value: Disabled
        description: Disable the censor in VoiceMod
csharpMethods:
  - VoiceModCensorOn
  - VoiceModCensorOff
---


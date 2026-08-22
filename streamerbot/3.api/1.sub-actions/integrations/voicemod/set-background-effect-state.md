---
title: Set Background Effect State
description: Modify the current state of background effects in VoiceMod
version: 0.1.8
parameters:
  - name: State
    type: Select
    description: Select the new background effect state to set in VoiceMod
    required: true
    options:
      - value: Enabled
        description: Enable background effects in VoiceMod
      - value: Disabled
        description: Disable background effects in VoiceMod
      - value: Toggle
        description: Toggle the current background effect state in VoiceMod
csharpMethods:
  - VoiceModBackgroundEffectOn
  - VoiceModBackgroundEffectOff
---


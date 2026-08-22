---
title: Set Voice Changer State
description: Modify the current Voice Changer State in VoiceMod
version: 0.1.8
parameters:
  - name: State
    type: Select
    description: Select the new Voice Changer state to set in VoiceMod
    required: true
    options:
      - value: Enabled
        description: Enable the Voice Changer State in VoiceMod
      - value: Disabled
        description: Disable the Voice Changer State in VoiceMod
      - value: Toggle
        description: Toggle the current Voice Changer State in VoiceMod
csharpMethods:
  - VoiceModVoiceChangerOn
  - VoiceModVoiceChangerOff
---

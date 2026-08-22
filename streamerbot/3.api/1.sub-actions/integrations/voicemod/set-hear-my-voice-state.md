---
title: Set Hear My Voice State
description: Modify the Hear My Voice State in VoiceMod
version: 0.1.8
parameters:
  - name: State
    type: Select
    description: Select the new Hear My Voice state to set in VoiceMod
    required: true
    options:
      - value: Enabled
        description: Enable the Hear My Voice state in VoiceMod
      - value: Disabled
        description: Disable the Hear My Voice state in VoiceMod
      - value: Toggle
        description: Toggle the current Hear My Voice state in VoiceMod
csharpMethods:
  - VoiceModHearMyVoiceOn
  - VoiceModHearMyVoiceOff
---


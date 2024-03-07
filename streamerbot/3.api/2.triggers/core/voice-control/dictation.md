---
title: Dictation
description: Trigger for a Voice Control Dictation
version: 0.2.0
variables:
  - name: spokenText
    type: string
    description: The full spoken phrase detected, *including the trigger phrase*
  - name: spokenTextConfidence
    type: number
    description: Voice Recognition confidence raw value
  - name: spokenTextConfidencePercent
    type: number
    description: Confidence value as a percentage
  - name: altPhraseText#
    type: string
    description: The text of an alternative phrase
  - name: altPhraseConfidence#
    type: number
    description: The confidence of an alternative phrase
  - name: altPhraseConfidencePercent#
    type: number
    description: The percentage of the confidence from an alternative phrase
  - name: spokenTextInput
    type: string
    description: Detected spoken phrase with trigger command stripped <br> (Only works with `Start` based commands)
  - name: spokenCommand
    type: string
    description: Detected Trigger command
---

## Parameters
::field-group
  ::field{name="Voice Control" type=Select}
    Select a command from the Voice Control tab.

    - Select `Any` to trigger on **any command**

    ::tip{color=amber}
    You can quickly register a voice command by clicking the `Create Voice Command` button!
    ::
  ::
::
# Command
Voice Control Command trigger.

## Details
This event triggers when a voice control command is used.

## Parameters
### `Voice Control`
Select any or a specific command from the Voice Control tab.

## Variables
:variables-description

Name | Description
----:|:------------
`spokenText` | The full spoken phrase detected, *including the trigger phrase*
`spokenTextConfidence` | Voice Recognition confidence raw value
`spokenTextConfidencePercent` | Confidence value as a percentage
`altPhraseText#` | The text of an alternative phrase
`altPhraseConfidence#` | The confidence of an alternative phrase
`altPhraseConfidencePercent#` | The percentage of the confidence from an alternative phrase
`spokenTextInput` | Detected spoken phrase with trigger command stripped <br> (Only works with `Start` based commands)
`spokenCommand` | Detected Trigger command
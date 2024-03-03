---
title: Speak
description: Send a message with text-to-speech (TTS) using Speaker.bot
variables:
  - name: success
    description: Was the request successful?
    type: bool
    value: true
  - name: speechFile
    description: The file containing the speech audio, or `null` if it doesn't exist
    type: string
  - name: duration
    description: The duration of the speech, when the delay option is used
    type: number
---

:image-preview

:read-more{to="/guide/integrations/speakerbot"}

## Parameters
::field-group
  ::field{name="Voice Alias" type=Text required}
  The name of the voice alias to use.
  ::

  ::field{name="Pass Through Bad Word Filter" type=Toggle}
  Toggle the bad word filter on or off.
  ::

  ::field{name="Silent" type=Toggle}
  Play the TTS silently

  Can be used with the delay option if you want to wait before the TTS is finished, but don't have the audio.
  ::

  ::field{name="Delay" type=Toggle}
  Wait for TTS to complete before continuuing execution of the current action
  ::

  ::field{name="Message" type=Text required}
  The message content to send to Speaker.bot.
  ::
::
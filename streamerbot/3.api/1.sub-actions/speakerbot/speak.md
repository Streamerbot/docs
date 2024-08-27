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
  Processes the TTS only

  Enabling this will cause Speaker.bot to only process the TTS, and not play it.  The `speechFile` argument will contain the full path to the processed audio file that can be played either in OBS, or using the Play Sound sub-action.
  ::

  ::field{name="Delay" type=Toggle}
  Wait for TTS to be processed and finish playing before continuing execution of the current action.  There is a hard limit of 30s on a timeout to prevent stuck queues.
  ::

  ::field{name="Message" type=Text required}
  The message content to send to Speaker.bot.
  ::
::
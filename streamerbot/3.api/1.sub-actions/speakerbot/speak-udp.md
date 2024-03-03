---
title: Speak (UDP)
description: Send a message with text-to-speech (TTS) using Speaker.bot via UDP
variables: []
csharpMethods:
  - TtsSpeak
---

:image-preview

:read-more{to="/guide/integrations/speakerbot"}

## Parameters
::field-group
  ::field{name="Voice Alias" type=Text required}
  The name of the voice alias to use
  ::

  ::field{name="Pass Through Bad Word Filter" type=Toggle}
  Toggle the bad word filter on or off
  ::

  ::field{name="Message" type=Text required}
  The message content to send to Speaker.bot
  ::
::
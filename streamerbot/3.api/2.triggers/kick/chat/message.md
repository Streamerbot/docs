---
title: Kick Chat Message
description: Trigger for a Kick Chat Message
variables:
  - name: isInternal
    type: boolean
    description: |
      If message was sent via Streamer.bot sub-action or C#

      Messages from Streamer.bot Chat are not considered as internal since `0.2.5`
    value: True / False
commonVariables:
  - KickUser
  - KickChat
---

---
name: SetUserVar
title: SetUserVar
description: Deprecated method to set a user variable
deprecated: 0.2.0
parameters:
  - name: varName
    import: core/globals/name
  - name: persisted
    import: core/globals/persisted
---

::warning
**This method is deprecated as of Streamer.bot v0.2.0**
<br>
Please use the [Twitch](/api/csharp/methods/twitch/globals/set-twitch-user-var) and [YouTube](/api/csharp/methods/youtube/globals/set-youtube-user-var) methods to set user variables specific to those platforms.
::
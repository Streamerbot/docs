---
title: Create Clip
description: Create a 30-second Twitch Clip
variables:
  - name: createClipSuccess
    type: bool
    description: Boolean result of the request
    value: True/False
  - name: createClipId
    type: string
    description: String identifier of the created clip
    value: AwkwardHelplessSalamanderSwiftRage
  - name: createClipCreatedAt
    type: string
    description: Timestamp of clip creation
    value: 7/11/2022 3:01:53 AM
  - name: createClipUrl
    type: string
    description: Full URL to the created clip
    value: https://clips.twitch.tv/AwkwardHelplessSalamanderSwiftRage
csharpMethods:
  - CreateClip
---

::warning
**Twitch API restrictions**
- The generated clip will always be 30 seconds in length
- The clip title will match your stream title at the time of creation

  To make your own changes to the clip duration and/or title, you can manually edit the clip later.
::

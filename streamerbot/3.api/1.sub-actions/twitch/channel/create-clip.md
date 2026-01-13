---
title: Create Clip
description: Create a Twitch Clip
parameters:
  - name: Clip Title
    type: string
    description: If blank, will match the stream title at the time of creation.
  - name: Duration
    type: int
    default: 30
    description: Clip duration in seconds (min. 5, max 60).
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

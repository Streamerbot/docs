---
title: Create Stream Marker
description: Trigger creation of a Stream Marker on Twitch
parameters:
  - name: Description
    type: Text
    description: |
      Write the description of your Stream Marker
variables:
  - name: streamMarkerSuccess
    type: bool
    description: The status of the sub-action request
    value: True/False
  - name: streamMarkerId
    type: string
    description: Id of the marker
    value: 8d25fc8f611f8aa57ae1eac3ad4b9c99
  - name: streamMarkerCreatedAt
    type: DateTime
    description: Time when the marker was set
    value: 01.01.0001 00:00:00
  - name: streamMarkerDescription
    type: string
    description: Description which was used for the marker
    value: This is a test marker
  - name: streamMarkerPosition
    type: int
    description: Position of the marker in the vod in seconds
    value: 42
csharpMethods:
  - CreateStreamMarker
---

You can use this to signify an important event, or as a reminder for a point in the stream you'd like to review in your VOD at a later time.

::warning
Stream Markers are only available if you have VODs enabled on your channel!
::
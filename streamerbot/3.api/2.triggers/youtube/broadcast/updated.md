---
title: Broadcast Updated
description: Trigger for YouTube broadcast changes
variables:
  - name: id
    type: string
    description: The unique ID of this broadcast
  - name: title
    type: string
    description: The title of this broadcast
    example: My Cool Stream
  - name: description
    type: string
    description: The description of this broadcast
    example: Check out all the cool stuff on my stream!
  - name: privacy
    type: string
    description: The privacy settings of this broadcast
commonVariables:
  - YouTubeBroadcaster
---
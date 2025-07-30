---
title: Guest Star Settings Update
description: Trigger for when the Guest Star settings get updated
version: 0.2.3
variables:
  - name: isModeratorSendLiveEnabled
    type: bool
    description: flag determining if Guest Star moderators have access to control whether a guest is live once assigned to a slot
    value: True/False
  - name: slotCount
    type: int
    description: number of slots the Guest Star call interface will allow the host to add to a call (between 1 and 6)
    value: 1
  - name: isBrowserSourceAudioEnabled
    type: bool
    description: flag determining if Browser Sources subscribed to sessions on this channel should output audio
    value: True/False
  - name: groupLayout
    type: string
    description: layout of the guests within a browser source
    value: tiled, screenshare, horizontal, vertical
commonVariables:
  - TwitchBroadcaster
---

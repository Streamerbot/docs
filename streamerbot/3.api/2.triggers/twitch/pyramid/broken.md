---
title: Pyramid Broken
description: Trigger for when a Twitch Pyramid is Broken
twitchService: Chat Client
variables:
  - name: totalPyramidsBroken
    type: number
    description: The total amount of pyramids the user has broken
    value: 8
  - name: pyramidWidth
    type: number
    description: The total amount of pyramid layers
    value: 3
  - name: pyramidEmote
    type: string
    description: The emote that was used in the pyramid
    value: Kappa
  - name: pyramidOwnerId
    type: string
    description: The user id of the person who initiated the pyramid
  - name: pyramidOwnerUsername
    type: string
    description: The user name of the person who initiated the pyramid
    value: twitchuser123
  - name: pyramidOwnerDisplayName
    type: string
    description: The display name of the person who initiated the pyramid
    value: TwitchUser123
commonVariables:
  - TwitchUser
---

::callout{color=amber icon=i-mdi-lightbulb}
The user variables are for the person who destroyed the pyramid.
::
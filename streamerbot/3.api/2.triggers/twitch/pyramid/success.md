---
title: Pyramid Success
description: Trigger for when a Twitch Pyramid is Succesfully created
twitchService: Chat Client
variables:
  - name: totalPyramids
    type: number
    description: The total amount of pyramids the user has made
    value: 8
  - name: pyramidWidth
    type: number
    description: The total amount of pyramid layers
    value: 3
  - name: pyramidEmote
    type: string
    description: The emote that was used in the pyramid
    value: Kappa
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
---
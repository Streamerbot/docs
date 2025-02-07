---
title: Send Shoutout
description: Send a shoutout to a user on Twitch
parameters:
  - name: User Login
    type: String
    required: true
    description: User login name or a variable like `%userName%`
variables:
  - name: shoutoutSuccess
    type: bool
    description: |
        - `True` - Shoutout was successfully made
        - `False` - Shoutout failed
        Reasons why a shoutout can fail:
        - You, the broadcaster, is currently not live
        - A shoutout is currently still on-going. 2 minutes per shoutout
        - A shoutout was already done for the specified person in the last hour
    value: true
csharpMethods:
  - TwitchSendShoutoutByLogin
  - TwitchSendShoutoutById
---

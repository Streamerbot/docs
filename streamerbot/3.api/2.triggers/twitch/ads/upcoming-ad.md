---
title: Upcoming Ad
description: Trigger for an upcoming Twitch Ad Run
version: 0.2.3
twitchService: PubSub
variables:
  - name: minutes
    type: number
    description: The number of minutes until the ad run will start
    value: 5
  - name: nextAdAt
    type: DateTime
    description: The exact date and time that the next ad run will start
    value: '2024-03-03 01:10:20'
  - name: snoozesLeft
    type: number
    description: The maximum number of snoozes left
    value: 3
  - name: adLength
    type: number
    description: The length of the upcoming ad run, in seconds
    value: 150
---

::tip
This trigger runs at 1 minute intervals starting at 5 minutes until the upcoming ad
::
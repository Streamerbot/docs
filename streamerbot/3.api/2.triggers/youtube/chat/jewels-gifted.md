---
title: Jewels Gifted
description: Trigger for a when jewels have been spent to send a gift to the broadcaster
version: 1.0.5
variables:
  - name: publishedAt
    type: DateTime
    description: The time the message was published at
    value: 5/8/2026 12:00:00 PM
  - name: gift.jewelsAmount
    type: number
    description: The amount of Jewels redeemed for the gift
    value: 10
  - name: gift.name
    type: string
    description: The name of the gift
    value: Thumbs up
  - name: gift.url
    type: string
    descripton: The URL of the gift asset
    value: 'https://www.gstatic.com/youtube/img/pdg/gift/assets/keep_it_up.png'
  - name: gift.durationInSeconds
    type: string
    description: The number of seconds to display the gift URL
    value: 3
  - name: gift.durationInNanoSeconds
    type: string
    description: The number of nanoseconds to display the gift URL
    value: 0
  - name: gift.hasVisualEffect
    type: boolean
    description: Indicates if the gift has a visual effect
    value: False
  - name: gift.isCombo
    type: boolean
    description: Indicates if this gift is part of a combo
    value: False
  - name: gift.comboCount
    type: number
    description: What combo level the gift is
    value: 1
  - name: gift.altText
    type: string
    description: A text string that describes the gift
    value: Thumbs up
  - name: gift.altTextLanguage
    type: string
    description: The language of the `gift.altText`
    value: en_US
commonVariables:
  - YouTubeUser
  - YouTubeBroadcast
  - YouTubeBroadcaster
---

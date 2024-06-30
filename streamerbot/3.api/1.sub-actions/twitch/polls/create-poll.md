---
title: Create Poll
description: Create a Twitch poll
parameters:
  - name: Title
    type: String
    required: true
    description: the poll's title
  - name: Choices
    type: String
    required: true
    description: Poll choices (min. 2, max. 5)
  - name: Channel Points Per Vote
    type: Int
    required: false
    description: Set Channel Points for extra votes
  - name: Duration
    type: Int
    required: false
    description: Set poll duration in seconds
variables:
  - name: pollId
    type: string
    description: the ID of the poll
    value: 6bac1033-996d-4798-a688-b4df93434d6f
  - name: success
    type: bool
    description: indicator whether the poll has been created successfully or not
    value: True/False
csharpMethods:
  - TwitchPollCreate
---

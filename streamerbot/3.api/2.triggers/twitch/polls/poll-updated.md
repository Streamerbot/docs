---
title: Poll Updated
description: Trigger for when a Twitch Poll is Updated
version: 0.0.50
twitchService: EventSub
variables:
  - name: poll.Title
    type: string
    description: The poll's title
    value: "Do you like coffee or energy drinks more?"
  - name: poll.Id
    type: string
    description: Twitch's internal id for the poll
    value: f76ddfef-8654-4fd1-9dda-b377a73ed9ef
  - name: poll.StartedAt
    type: DateTime
    description: The timestamp that the poll was created
    value: 8/4/2023 10:56:06 AM
  - name: poll.Duration
    type: int
    description: The duration of the poll in seconds
    value: 300
  - name: poll.DurationRemaining
    type: int
    description: The remaining time in milliseconds
    value: 300
  - name: poll.choices.count
    type: int
    description: The number of choices in the poll
    value: 3
  - name: poll.choice#.title
    type: string
    description: The title of this choice
    value: Choice 1
  - name: poll.choice#.votes
    type: int
    description: The number of regular votes of this choice
    value: 10
  - name: poll.choice#.rewardVotes
    type: int
    description: The total number of reward based votes of this choice
    value: 7
  - name: poll.choice#.totalVotes
    type: int
    description: The total number of votes for this choice
    value: 17
  - name: poll.votes
    type: int
    description: The total number of regular votes
    value: 30
  - name: poll.rewardVotes
    type: int
    description: The total number of reward based votes
    value: 19
  - name: poll.totalVotes
    type: int
    description: The total number of votes
    value: 49
  - name: poll._json
    type: string
    description: All the variables in a JSON Object
commonVariables:
  - TwitchBroadcaster
---

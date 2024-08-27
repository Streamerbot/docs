---
title: Get Active Poll
description: Check if a poll is currently active
version: 0.2.5
variables:
  - name: active
    type: bool
    description: Indicator whether an active poll is running
    value: True
  - name: poll.Title
    type: string
    description: The poll's title
    value: Which game should we play next stream?
  - name: poll.Id
    type: string
    description: Twitch's internal id for the poll
    value: f76ddfef-8654-4fd1-9dda-b377a73ed9ef
  - name: poll.StartedAt
    type: DateTime
    description: The timestamp that the poll was created
    value: 8/4/2023 10:56:06 AM
  - name: poll.EndsAt
    type: DateTime
    description: The timestamp when the poll will end
    value: 8/4/2023 10:56:06 AM
  - name: poll.Duration
    type: int
    description: The total duration of the poll in seconds
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
  - name: poll.choice#.id
    type: string
    description: The id of this choice
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
---

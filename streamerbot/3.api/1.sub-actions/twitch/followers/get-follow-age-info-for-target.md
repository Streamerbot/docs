---
title: Get Follow Age Info for Target
description: Get the follow age from a Twitch user
parameters:
  - name: Source Type
    type: Select
    required: true
    description: |
        Select from which source you want to get the follow age:
        - `User`: User that invoked the action e.g. a raid leader, subscriber, point redeemer etc.
        - `From Input`: This will take the next word proceeding the trigger as the username to lookup. This user does not have to be present in the channel
        - `Variable`: Use the content of an existing variable as the target
  - name: Variable
    type: string
    description: Argument name if `Source Type` is `Variable`
variables:
  - name: isFollowing
    type: bool
    description: Whether the user is following the channel
    value: `True`/`False`
  - name: followDate
    type: string
    description: The date the user followed
    value: Saturday, 17 August 2024
  - name: followAgeLong
    type: string
    description: How long the user has been following in a long format
    value: 1 year, 10 months, 5 days, 22 hours, 3 minutes, 25 seconds
  - name: followAgeShort
    type: string
    description: How long the user has been following in a short format
    value: 1y, 10m, 5d, 22h, 3m, 25s
  - name: followAgeDays
    type: string
    description: The total number of days the user has been following
    value: 4,149
  - name: followAgeMinutes
    type: string
    description: The total number of minutes the user has been following
    value: 5,975,949
  - name: followAgeSeconds
    type: string
    description: The total number of seconds the user has been following
    value: 358,556,951
  - name: followUser
    type: string
    description: The users display name
    value: StreamerDotBot
  - name: followUserName
    type: string
    description: The user's login name
    value: streamerdotbot
  - name: followUserId
    type: string
    description: The user's Twitch id
    value: 718933593
  - name: followAge.years
    type: int
    description: Amount of years followed
    value: 11
  - name: followAge.months
    type: int
    description: Amount of months followed (rest from years)
    value: 4
  - name: followAge.days
    type: int
    description: Amount of days followed (rest from months)
    value: 14
  - name: followAge.hours
    type: int
    description: Amount of hours followed (rest from days)
    value: 23
  - name: followAge.minutes
    type: int
    description: Amount of minutes followed (rest from hours)
    value: 9
  - name: followAge.seconds
    type: int
    description: Amount of seconds followed (rest from minutes)
    value: 11
---

## C# Usage
:csharp-method

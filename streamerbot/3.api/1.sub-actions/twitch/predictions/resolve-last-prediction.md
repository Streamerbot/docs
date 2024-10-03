---
title: Resolve Last Prediction
description: Resolves the last active prediction
version: 0.2.5
parameters:
  - name: Winning Index
    type: number
    description: Specify the zero-based index of the outcome to use as the winning outcome (`%variables%` **ARE** supported)
    required: true
    value: 1
variables:
  - name: active
    type: bool
    description: Indicator whether an active prediction is running (and not locked yet)
    value: True
  - name: prediction.Id
    type: string
    description: Twitch's internal id for the prediction
    value: 926596a5-c404-4179-8bba-faf8b4f49151
  - name: prediction.CreatedAt
    type: DateTime
    description: The timestamp that the prediction was created
    value: 8/4/2023 10:56:06 AM
  - name: prediction.Title
    type: string
    description: The title of the prediction
    value: My prediction title
  - name: prediction.PredictionWindow
    type: number
    description: The duration of the prediction (in seconds)
    value: 60
  - name: prediction.winningIndex
    type: number
    description: Index number of the winning prediction option
    value: 0
  - name: prediction.winningOutcome.id
    type: string
    description: The id for the winning outcome
    value: 0d7047e8-1a24-4cb1-8cdd-31d3dc715130
  - name: prediction.winningCutcome.title
    type: string
    description: The title for the winning outcome
    value: Outcome 1
  - name: prediction.winningOutcome.users
    type: number
    description: How many users voted for the winning outcome
    value: 20
  - name: prediction.winningOutcome.points
    type: number
    description: The amount of channel points used for the winning outcome
    value: 1200
  - name: prediction.winningOutcome.color
    type: string
    description: In capital letters the color name for the winning outcome
    value: BLUE
  - name: prediction.outcome#.id
    type: string
    description: The id for this outcome
    value: 0d7047e8-1a24-4cb1-8cdd-31d3dc715130
  - name: prediction.outcome#.title
    type: string
    description: The title for this outcome
    value: Outcome 1
  - name: prediction.outcome#.users
    type: number
    description: How many users voted for this outcome
    value: 20
  - name: prediction.outcome#.points
    type: number
    description: The amount of channel points used for this outcome
    value: 1200
  - name: prediction.outcome#.color
    type: string
    description: In capital letters the color name for this outcome
    value: BLUE
  - name: success
    type: boolean
    description: Whether or not the prediction was successfully resolved
    value: true
csharpMethods:
  - TwitchPredictionResolve
---

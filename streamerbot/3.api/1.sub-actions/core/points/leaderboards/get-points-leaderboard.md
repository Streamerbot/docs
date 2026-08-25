---
title: Get Points Leaderboard
description: Fetch the points leaderboard for a specific point definition
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to fetch the leaderboard for
  - name: Count
    type: number
    required: true
    default: None
    description: The number of top users to fetch
  - name: Offset
    type: number
    required: true
    default: 0
    description: The starting point for fetching the leaderboard (0-indexed, supports variables)
csharpMethods:
  - GetLeaderboard
---
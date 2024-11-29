---
title: Statistics Updated
description: Trigger for changes to YouTube broadcast stats
variables:
  - name: likeCount
    type: number
    description: The total number of likes for this broadcast
    value: 99
  - name: dislikeCount
    type: number
    description: The total number of dislikes for this broadcast
    value: 0
  - name: viewCount
    type: number
    description: The total number of views for this broadcast
    value: 9001
  - name: favoriteCount
    type: number
    description: (Deprecated) - Number of times this broadcast has been favorited
    value: 25
  - name: commentCount
    type: number
    description: Number of comments this broadcast has
    value: 42
  - name: concurrentViewers
    type: number
    description: |
      The number of viewers currently watching this broadcast

      Broadcaster needs to have the viewcount enabled for this broadcast to represent the correct value.
    value: 42
commonVariables:
  - YouTubeBroadcast
---
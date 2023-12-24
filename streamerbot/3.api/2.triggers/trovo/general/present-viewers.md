---
title: Present Viewers
description: Trigger for the Trovo present viewers event
variables:
  - name: title
    type: string
    description: The stream title
  - name: audienceType
    type: string
    description: The current audience type
  - name: categoryId
    type: string
    description: The current category ID
  - name: categoryName
    type: string
    description: The current category name
  - name: viewerCount
    type: number
    description: The current viewer count
  - name: subscribers
    type: number
    description: The amount of subscribers
  - name: followers
    type: number
    description: The amount of followers
  - name: startedAt
    type: DateTime
    description: The epoch time the stream has stated
  - name: isLive
    type: boolean
    description: Boolean for current streaming status `True`/`False`
  - name: users
    type: dictionary
    description: A C# Dictionary list of usernames present in chat <br> Each user present will get [the following data](#users-dictionary)
commonVariables:
  - TrovoUser
  - TrovoDictionaryUsers
---

## Details
The present viewers trigger runs every 1-10 minutes, by default every 5 minutes. It'll give a list of all the users in your stream, this data can be only used in C#.
---
title: Stream Online
description: Trigger for when your stream on Twitch is started
version: 0.1.17
twitchService: EventSub
variables:
  - name: startedAt
    type: DateTime
    description: The date and time that the stream was ended
    value: 8/4/2023 10:56:06 AM
  - name: game
    type: string
    description: The category name
    value: Just Chatting
  - name: gameId
    type: number
    description: The category id
    value: 509658
  - name: tagCount
    type: number
    description: The number of tags
    value: 2
  - name: tag#
    type: string
    description: Each individual tag
  - name: tags
    type: List<string>
    description: A C# accessible list of tags
  - name: tagsDelimited
    type: string
    description: A comma delimited string of the tags
---
---
title: Poll Closed
description: Trigger that occurs when a poll is closed
variables:
  - name: poll.question
    type: string
    description: The question asked
  - name: poll.totalVotes
    type: int
    description: The total number of votes cast
  - name: poll.options.count
    type: int
    description: The number of available options
  - name: poll.option0.text
    type: string
    description: The first poll option listed
  - name: poll.option0.votes
    type: int
    description: The number of votes cast for the first option
  - name: poll.option1.text
    type: string
    description: The second poll option listed
  - name: poll.option1.votes
    type: int
    description: The number of votes cast for the second option
  - name: poll.winningOption.text
    type: string
    description: The option that received the most votes OR if there is a tie, the first listed option that tied
  - name: poll.winningOption.votes
    type: int
    description: The number of votes cast for the winning option
commonVariables:
  - YouTubeUser
  - YouTubeBroadcast
  - YouTubeBroadcaster
---

::note
  **If you have more than two options they will appear as poll.option2.text, poll.option2.votes, poll.option3.text, poll.option3.votes, and so on**
::

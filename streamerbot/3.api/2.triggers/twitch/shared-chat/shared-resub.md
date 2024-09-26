---
name: Shared Resub
description: Triggered when a user resubscribes in the shared chat
twitchService: EventSub
version: 0.2.5
  - name: tier
    type: string
    description: The subscription tier<br>`prime`, `tier 1`, `tier 2`, `tier 3`
    value: tier 1
  - name: monthStreak
    type: number
    description: The current subscription streak of the user
    value: 5
  - name: cumulative
    type: number
    description: The amount of cumulative months that the user is subscribed for
    value: 2
commonVariables:
  - TwitchUser
  - TwitchChat
 ---
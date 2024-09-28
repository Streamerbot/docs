---
name: Shared Community Sub Gift
description: Triggered when a user gifts community subscriptions in the shared chat
twitchService: EventSub
version: 0.2.5
  - name: tier
    type: string
    description: The subscription tier<br>`prime`, `tier 1`, `tier 2`, `tier 3`
    value: tier 1
  - name: anonymous
    type: boolean
    description: Returns whether or not the sub was gifted anonymously
    value: False
  - name: gifts
    type: number
    description: The number of subscriptions in this gift bomb
    value: 6
  - name: totalGifts
    type: number
    description: The total amount of subscriptions that the user has gifted
    value: 24
  - name: bonusGifts
    type: boolean
    version: 0.2.5
    description:  A boolean value if Twitch adds additional subs to the Gift Bomb.
    value: true
commonVariables:
  - TwitchUser
  - TwitchChat
 ---

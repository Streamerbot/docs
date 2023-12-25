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
    type: bool
    description: Boolean for current streaming status
    value: true
  - name: users
    type: Dictionary<TrovoUser>
    description: A C# accessible list of users present in chat
    variables:
      - name: id
        type: string
        description: The user id of the user
        value: trovo_678296378
      - name: userName
        type: string
        description: The user name of the user
        value: trovouser123
      - name: display
        type: string
        description: The display name of the user
        value: TrovoUser123
      - name: role
        type: number
        description: The role of the user<br>1=`Viewer`, 2=`VIP`, 3=`Moderator`, 4=`Broadcaster`
        value: 1
      - name: isSubscribed
        type: bool
        description: Is the user subscribed?
        value: true
      - name: isModerator
        type: bool
        description: Is the user a moderator?
        value: true
commonVariables:
  - TrovoUser
---

## Details
The present viewers trigger runs every 1-10 minutes, by default every 5 minutes. It'll give a list of all the users in your stream, this data can be only used in C#.
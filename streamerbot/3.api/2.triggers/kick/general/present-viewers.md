---
title: Present Viewers
description: Trigger for the Kick present viewers event
variables:
  - name: isTest
    type: boolean
    description: Is this event a test?
  - name: isLive
    type: boolean
    description: Is the stream live?
    value: True
  - name: users
    type: List<Dictionary<string,object>>
    description: A C# accessible list of users present in chat
    children:
      - name: id
        type: string
        description: The user id of the user
        value: a126e8a8-43f7-4a14-8990-e8c3feea76d8
      - name: userName
        type: string
        description: The user name of the user
        value: kickuser123
      - name: display
        type: string
        description: The display name of the user
        value: KickUser123
      - name: role
        type: number
        description: The role of the user<br>1=`Viewer`, 2=`VIP`, 3=`Moderator`, 4=`Broadcaster`
        value: 1
      - name: isSubscribed
        type: boolean
        description: Is the user a subscriber?
        value: True
  - name: title
    type: string
    description: The title of the stream
    value: Super Awesome Kick Stream Title
  - name: viewerCount
    type: number
    description: The number of viewers currently present in the stream
    value: 69
  - name: startedAt
    type: DateTime
    description: The date and time when the stream started
    value: 7/19/2025 10:38:24 PM
  - name: categoryId
    type: string
    description: The category id of the stream
    value: 5787
  - name: categoryName
    type: string
    description: The category name of the stream
    value: Cats & Soup
  - name: categoryThumbnail
    type: string
    description: The category thumbnail of the stream
    value: https://files.kick.com/categories/5787/thumbnail
commonVariables:
  - KickBroadcaster
---

## Notes
The Kick present viewer acts more like a chat activity tracker. There is no "Live-Update" option for Kick as the API does not provide the viewer list.

Under the `Platforms > Kick > Settings`, you will find the options for the Present Viewers Trigger.

The slider behaves as a threshold. The timer runs every minute, and checks the current time minus the user's last active time, if this is less then the threshold, they are marked as present, otherwise they are marked as not present.  The trigger will be executed every minute.

The default setting is the slider set to `5` minutes.
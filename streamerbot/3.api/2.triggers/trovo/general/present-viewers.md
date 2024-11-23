---
title: Present Viewers
description: Trigger for the Trovo present viewers event
variables:
  - name: isTest
    type: boolean
    description: Is this event a test?
    value: True
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
    type: number
    description: The epoch time the stream has stated
    value: 1704063600
  - name: isLive
    type: bool
    description: Boolean for current streaming status
    value: true
  - name: users
    type: List<Dictionary<string,object>>
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
  - TrovoBroadcaster
---

## Details
This triggers every 1-10 minutes, default every 5 minutes.

## Notes
The present viewer tick will always happen, but you have the ability to have it "live update" from Trovo, or artificially mark someone as present.

Under the `Platforms > Trovo > Settings`, in the Present Viewers section, there are 2 settings, a `Live Update` check box, and a slider bar.

When `Live Update` is checked, the slider beneath it is how often this update will occur, between 1 and 10 minutes, this will also execute the action at this interval.

When Live Update is not checked, the slider next to it behaves as a threshold. The timer runs every minute, and checks the current time minus the user's last active time, if this is less then the threshold, they are marked as present, otherwise they are marked as not present.  The action will still be executed, but, it will occur every minute.

The default setting is `Live Update` not checked, and the slider set to `5` minutes.
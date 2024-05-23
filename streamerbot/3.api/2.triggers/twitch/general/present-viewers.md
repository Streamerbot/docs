---
title: Present Viewers
description: Trigger for the Twitch present viewers event
version: 0.0.50
twitchService: EventSub
variables:
  - name: isTest
    type: boolean
    description: Is this event a test?
    value: True
  - name: isLive
    type: boolean
    description: Is the stream live?
    value: True
  - name: users
    type: List<Dictionary<string, object>>
    description: A C# accessible list of users present in chat
    variables:
      - name: id
        type: string
        description: The user id of the user
        value: 12345678
      - name: userName
        type: string
        description: The user name of the user
        value: twitchuser123
      - name: display
        type: string
        description: The display name of the user
        value: TwitchUser123
      - name: role
        type: number
        description: The role of the user<br>1=`Viewer`, 2=`VIP`, 3=`Moderator`, 4=`Broadcaster`
        value: 1
      - name: isSubscribed
        type: boolean
        description: Is the user subscribed?
        value: true
      - name: title
        type: string
        description: Stream title, if the user is currently live
        value: 'My Stream'
      - name: gameId
        description: Stream game ID, if the user is currently live
        type: string
        value: '2491012'
      - name: gameName
        description: Stream game name, if the user is currently live
        type: string
        value: 'Just Chatting'
      - name: viewerCount
        description: Stream viewer count, if the user is currently live
        type: number
        value: 12
      - name: startedAt
        description: Stream start time, if the user is currently live
        type: DateTime
        value: 8/4/2023 10:56:06 AM
---

## Details
This triggers every 1-10 minutes, default every 5 minutes.

## Notes
The present viewer tick will always happen, but you have the ability to have it "live update" from twitch, or artificially mark someone as present.

Under the Present Viewer action selector, there are 2 settings, a `Live Update` check box, and a slider bar.

When Live Update is checked, the slider next to it is how often this update will occur, between 1 and 10 minutes, this will also still execute the action at this interval.

When Live Update is not checked, the slider next to it behaves as a threshold. The timer runs every minute, and checks the current time minus the user's last active time, if this is less then the threshold, they are marked as present, otherwise they are marked as not present.  The action will still be executed, but, it will occur every minute.

The default setting is `Live Update` not checked, and the slider set to `5` minutes.  To have the same functionality as `v0.1.12` and earlier, enable `Live Update` and make sure the slider is set to `5` minutes.
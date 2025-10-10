---
title: Present Viewers
description: Trigger for YouTube viewer changes
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
        value: youtubeuser123
      - name: display
        type: string
        description: The display name of the user
        value: YouTubeUser123
      - name: role
        type: number
        description: The role of the user<br>1=`Viewer`, 2=`VIP`, 3=`Moderator`, 4=`Broadcaster`
        value: 1
      - name: isSubscribed
        type: boolean
        description: Is the user a member?
        value: True
commonVariables:
  - YouTubeBroadcaster
---

## Notes
The YouTube present viewer acts more like a chat activity tracker. There is no "Live-Update" option for YouTube as the API does not provide the viewer list.

Under the `Platforms > YouTube > Settings`, you will find the options for the Present Viewers Trigger.

The slider behaves as a threshold. The timer runs every minute, and checks the current time minus the user's last active time, if this is less then the threshold, they are marked as present, otherwise they are marked as not present.  The trigger will be executed every minute.

The default setting is the slider set to `5` minutes.
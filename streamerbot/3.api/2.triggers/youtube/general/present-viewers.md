---
title: Present Viewers
description: Trigger for YouTube viewer changes
variables:
  - name: title
    type: string
    description: The title of the stream
    value: My stream title
  - name: isLive
    type: boolean
    description: Is the stream live?
    value: True
  - name: users
    type: Dictionary<YouTubeUser>
    description: A C# accessible list of users present in chat
    variables:
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
        description: Is the user subscribed?
        value: True
commonVariables:
  - YouTubeBroadcaster
---
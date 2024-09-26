---
name: Shared Announcement
description: Triggered when an announcement is shared between both chats
twitchService: EventSub
version: 0.2.5
variables:
    name: fromSharedChat
    type: boolean
    description: Returns whether or not the action came from the shared chat
    value: True
    name: role
    type: string
    description: Returns the role of who posted the announcement
    value: Broadcaster
    name: isSubscribed
    type: boolean
    description: Returns whether or not the person who posted the announcement is subscribed
    value: True
    name: message
    type: string
    description: Returns the entire text of the announcement
    value: "This is a super important announcement!!"    
    name: messageStripped
    type: string
    description: Returns the text of the announcement, with emotes removed
    value: "This is a super important announcement!!"  
    name: announceColor
    type: string
    description: Returns the color of the Shared Announcement
    value: Green
commonVariables:
  - TwitchChat
  - TwitchUser
 ---
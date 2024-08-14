---
title: YouTube Broadcast Variables
navigation.title: YouTube Broadcast
variables:
  - name: broadcast.id
    type: string
    description: The ID of the broadcast the message was sent from
    value: UCI9-KG2xoyh5z-g41IL2jqf
  - name: broadcast.title
    type: string
    description: The title of the broadcast the message was sent from
    value: Really cool stream title
  - name: broadcast.description
    type: string
    description: The description of the broadcast the message was sent from
    value: Super cool YouTube Stream happening now!
  - name: broadcast.privacy
    type: string
    description: |
      The privacy setting of the broadcast the message was sent from

      Valid values are `public`, `unlisted`, `private`
    value: public
  - name: broadcast.status
    type: string
    description: |
      The online status of the broadcast the message was sent from
      
      Possible values are, `complete`, `created`, `live`, `liveStarting`, `ready`, `revoked`, `testStarting`, `testing` 
    value: live
  - name: broadcast.publishedAt
    type: DateTime
    description: When the YouTube broadcast was first published on YouTube
    value: 12/21/2023 9:25:21 AM
  - name: broadcast.defaultLanguage
    type: string
    description: The default language code for the YouTube Broadcast's Title and Description
    value: en
  - name: broadcast.defaultAudioLanguage
    type: string
    description: The default language code for the YouTube Broadcast's Stream
    value: en
  - name: broadcast.tags
    type: string
    description: The tags that are set for the YouTube Broadcast as a comma delimited string, and these tags are case sensitive.
    value: Horizontal,Gaming
---

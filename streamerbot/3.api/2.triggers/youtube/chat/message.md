---
title: Message
description: Trigger for incoming YouTube chat messages
variables:
  - name: messageId
    type: string
    description: The ID of the message
    value: LCC.EhwKGkNPclgwSzZENlljREZUODZzd0FkbTJ3QXBR
  - name: message
    type: string
    description: The message contents
    value: Hello, world!
  - name: publishedAt
    type: DateTime
    description: The time the message was sent at
    value: 8/4/2023 10:56:06 AM
  - name: userIsSponsor
    type: boolean
    description: Indicates whether the viewer is a current channel member or not
    value: True
  - name: parts
    type: string
    description: JSON Format that separates each block of text from the emotes within a chat message
    value: '[{`"text"`:"hello"},{`"emoji"`:":chillwdog:","image":"https://yt3.ggpht.com/Ir9mDxzUi0mbqyYdJ3N9Lq7bN5Xdt0Q7fEYFngN3GYAcJT_tccH1as1PKmInnpt2cbWOam4=w24-h24-c-k-nd","startIndex":6,"endIndex":16,"text":":chillwdog:"},{`"text"`:"world"}]'
  - name: emotes
    type: string
    description: JSON Format that separates each emote, providing name, start/end index, and imageURL
    value: '[{"name":":chillwdog:","startIndex":6,"endIndex":16,"imageUrl":"https://yt3.ggpht.com/Ir9mDxzUi0mbqyYdJ3N9Lq7bN5Xdt0Q7fEYFngN3GYAcJT_tccH1as1PKmInnpt2cbWOam4=w24-h24-c-k-nd"},{"name":":chillwcat:","startIndex":52,"endIndex":62,"imageUrl":"https://yt3.ggpht.com/y03dFcPc1B7CO20zgQYzhcRPka5Bhs6iSg57MaxJdhaLidFvvXBLf_i4_SHG7zJ_2VpBMNs=w24-h24-c-k-nd"}]'
commonVariables:
commonVariables:
  - YouTubeUser
  - YouTubeBroadcaster
---

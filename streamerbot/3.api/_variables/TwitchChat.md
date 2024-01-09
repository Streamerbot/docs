---
title: Twitch Chat Variables
navigation.title: Twitch Chat
variables:
  - name: msgId
    type: string
    description: Twitch's message identifier
    value: a126e8a8-43f7-4a14-8990-e8c3feea76d8
  - name: bits
    type: number
    description: The amount of bits donated
    value: 200
  - name: role
    type: number
    description: The role of the user<br>1=`Viewer`, 2=`VIP`, 3=`Moderator`, 4=`Broadcaster`
    value: 1
  - name: color
    type: string
    description: Hex value of the user's chat color
    value: '#e5e5e5'
  - name: colorR
    type: string
    description: The red in RGB of the user's chat color
    value: 229
  - name: colorG
    type: string
    description: The green in RGB of the user's chat color
    value: 229
  - name: colorB
    type: string
    description: The blue in RGB of the user's chat color
    value: 229
  - name: message
    type: string
    description: Text content of the chat message
    value: Hello!
  - name: messageStripped
    type: string
    description: The chat message with emotes stripped
    value: Hello!
  - name: messageCheermotesStripped
    type: string
    description: The chat message with cheer emotes stripped.
    value: Hello!
  - name: emoteCount
    type: number
    description: Number of emotes in the chat message
    value: 0
  - name: emotes
    type: List<TwitchEmote>
    description: A C# accessible list of emotes used in the chat message
    variables:
      - name: id
        type: number
        description: The id of the emote
        value: 25
      - name: type
        type: string
        description: From which source the emote came from
        value: Twitch
      - name: startIndex
        type: number
        description: On which letter the emote started
        value: 0
      - name: endIndex
        type: number
        description: On which letter the emote ended
        value: 4
      - name: imageUrl
        type: string
        description: The URL of an image from the emote
        value: https://static-cdn.jtvnw.net/emoticons/v2/25/default/dark/2.0
  - name: isHighlight
    type: boolean
    description: Is this message a Twitch Highlight?
    value: True
  - name: isAction
    type: boolean
    description: Is this message a `/me` action?
    value: True
  - name: isReply
    type: boolean
    description: Is this message a reply?
    value: True
  - name: reply.msgId
    type: string
    description: The message id of the reply
    value: a126e8a8-43f7-4a14-8990-e8c3feea76d8
  - name: reply.userId
    type: string
    description: The user id from the user who sent the reply
    value: 718933593
  - name: reply.userLogin
    type: string
    description: The user login from the user who sent the reply
    value: twitchuser123
  - name: reply.userName
    type: string
    description: The user name from the user who sent the reply
    value: TwitchUser123
  - name: reply.msgBody
    type: string
    description: The text content of the reply, **Spaces are replaced by `\s`**
    value: 'My\schat\smessage'
  - name: reply.threadMsgId
    type: string
    description: The message id of the thread
    value: a126e8a8-43f7-4a14-8990-e8c3feea76d8
  - name: reply.threadUserLogin
    type: string
    description: The user login name of the thread
    value: twitchuser123
  - name: firstMessage
    type: boolean
    description: Is this user a first time chatter?
    value: True
---
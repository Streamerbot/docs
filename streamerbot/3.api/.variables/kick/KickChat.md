---
title: Kick Chat Variables
navigation.title: Kick Chat
variables:
  - name: messageId
    type: string
    description: Kick's message identifier
    value: 1e984859-a29f-4dd3-b2fb-d13e70b6b4e8
  - name: message
    type: string
    description: Text content of the chat message
    value: Hello!
  - name: messageStripped
    type: string
    description: The chat message with emotes stripped
    value: Hello!
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
  - name: emoteCount
    type: number
    description: Number of emotes in the chat message
    value: 3
  - name: emotes
    type: List
    description: A C# accessible list of emotes used in the chat message
    children:
      - name: emotes.#.text
        type: string
        description: Plain text name of the emote
        value: emojiAngry
      - name: emotes.#.id
        type: number
        description: Unique identifier for the emote
        value: 1730753
      - name: emotes.#.url
        type: string
        description: URL of the emote image
        value: https://files.kick.com/emotes/1730753/fullsize
  - name: badgeCount
    type: number
    description: Number of badges the user has
    value: 1
  - name: badge
    type: List
    description: A C# accessible list of badges used in the chat message
    children:
      - name: badge.#.id
        type: string
        description: Plain text name of the badge
        value: broadcaster
      - name: badge.#.name
        type: string
        description: Unique identifier for the badge
        value: Broadcaster
      - name: badge.#.info
        type: string
        description: URL of the badge image
        value: https://files.kick.com/badges/broadcaster
  - name: rawInput
    type: string
    description: The message receieved in chat
  - name: rawInputEscaped
    type: string
    description: The message escaped
  - name: rawInputUrlEncoded
    type: string
    description: The message URL encoded
  - name: input.count
    type: number
    description: The number of words in the message received
  - name: input#
    type: string
    description: The `#` word of the message entered, spaces are delimiters and variable names are 0 indexed, so `input0` would give the first word, `input1` would give the second, and so on
  - name: inputEscaped#
    type: string
    description: The indexed word escaped
  - name: inputUrlEncoded#
    type: string
    description: The indexed word URL encoded
---
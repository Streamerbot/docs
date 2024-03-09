---
title: VStream Chat Variables
navigation.title: VStream Chat
variables:
  - name: messageId
    type: string
    description: VStream message ID
    value: chat_4ngvd3qbb780rakfe1vsmg90he
  - name: createdAt
    type: DateTime
    description: The date and time the message was created at
    value: 09/03/2024 12:13:15 AM
  - name: color
    type: string
    description: The HEX color
    value: #89e56f
  - name: colorR
    type: number
    description: The R value of the RGB color
    value: 137
  - name: colorG
    type: number
    description: The G value of the RGB color
    value: 229
  - name: colorB
    type: number
    description: The B value of the RGB color
    value: 111
  - name: message
    type: string
    description: Text content of the chat message
    value: Hello!
  - name: emojis
    type: List<Unknown>
    description: The list of emojis included
    value: "[]"
  - name: rawInput
    type: string
    description: The raw message sent to the chat
    value: Hello!
  - name: rawInputEscaped
    type: string
    description: The raw message sent to the chat escaped
    value: Hello!
  - name: rawInputUrlEncoded
    type: string
    description: The raw message sent to the chat url encoded
    value: Hello!
  - name: input#
    type: string
    description: A indexed word from the `rawInput`
    value: Hello!
  - name: inputEscaped#
    type: string
    description: A indexed word from the `rawInput` escaped
    value: Hello!
  - name: inputUrlEncoded#
    type: string
    description: A indexed word from the `rawInput` url encoded
    value: Hello!
---

::callout{icon="i-mdi-lightbulb" color=primary}
Change the `#` in the variables above to a number starting from 0. So for example: `input0`, `input1`, etc.
::
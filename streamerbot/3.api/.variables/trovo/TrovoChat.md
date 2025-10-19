---
title: Trovo Chat Variables
navigation.title: Trovo Chat
variables:
  - name: messageId
    type: string
    description: Trovo's message identifier
    value: 1701438166100574209_115023477_115023477_2887060856_1
  - name: message
    type: string
    description: Text content of the chat message
    value: Hello!
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
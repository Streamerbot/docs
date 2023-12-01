---
variables.summaryText: Trovo Chat
variables.summaryIcon: mdi:message-text
---

| Name | Description | Example |
|-----:|:------------|:--------|
`messageId` | Trovo's message identifier	| `1701438166100574209_115023477_115023477_2887060856_1`
`message` | Text content of the chat message | Hello!
`rawInput` | The raw message sent to the chat | Hello!
`rawInputEscaped` | The raw message sent to the chat escaped | Hello!
`rawInputUrlEncoded` | The raw message sent to the chat url encoded | Hello!
`input#` | A word from the `rawInput` | Hello!
`inputEscaped#` | A word from the `rawInput` escaped | Hello!
`inputUrlEncoded#` | A word from the `rawInput` url encoded | Hello!

::callout{icon="i-mdi-lightbulb" color=primary}
Change the `#` in the variables above to a number starting from 0. So for example: `input0`, `input1`, etc.
::
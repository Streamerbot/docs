---
variables.summaryText: Twitch Chat
variables.summaryIcon: mdi:message-text
---

| Name | Description | Example |
|-----:|:------------|:--------|
`msgId` | Twitch's message identifier | `a126e8a8-43f7-4a14-8990-e8c3feea76d8`
`role` | The role of the Twitch user | `1` (Viewer), `2` (VIP), `3` (Mod), `4` (Broadcaster)
`isSubscribed` | Is the user subscribed? | `True` / `False`
`color` | Hex value of user's chat color | `#e5e5e5`
`message` | Text content of the chat message | `Hello!`
`messageStripped` | The chat message with emotes stripped. | `Hello!`
`messageCheermotesStripped` | The chat message with cheer emotes stripped. | `Hello!`
`emoteCount` | Number of emotes in the chat message | `0`
`emotes` | Comma Separated list of Twitch emotes found.
`isHighlight` | Is this message a Twitch Highlight? | `True` / `False`
`isAction` | Is this message a `/me` action? | `True` / `False`
`isReply`| Is this message a reply? | `True` / `False`
`replyTo`| The username the message is replying to | `twitchuser123`
`firstMessage` | Is this user a first time chatter? | `True` / `False`
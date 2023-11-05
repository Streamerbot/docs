---
version: 0.1.14
---

# Bot Whispers
When someone sends the bot account a whisper.

## Notes
The user sending the whisper must have a **verified phone number** (see the **Phone Number setting** in your **Security and Privacy settings**).

The API may silently drop whispers that it suspects of violating Twitch policies, it will still indicate success even if the message is dropped.

Rate Limits: You may whisper to a maximum of **40 unique recipients per day**. Within the per day limit, you may whisper a maximum of 3 whispers per second and a maximum of 100 whispers per minute.

The maximum message lengths are:
* 500 characters if the user you're sending the message to hasn't whispered you before.
* 10,000 characters if the user you're sending the message to has whispered you before.

Messages that exceed the maximum length are truncated.

## Details
::list
- Twitch Service: `Chat Client`
::

## Variables
:variables-description

:variables{name=TwitchUser disclosure}
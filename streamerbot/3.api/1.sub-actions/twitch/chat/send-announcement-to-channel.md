---
title: Send Announcement to Channel
description: Send an announcement to your Twitch channel
parameters:
  - name: Preferred Account
    type: Select
    default: Bot
    required: true
    description: |
      Select the Twitch account to use when sending the announcement

      - `Bot`: Send the message from your [bot account](/guide/platforms/twitch#accounts)
      - `Broadcaster`: Send the announcement from your [broadcaster account](/guide/platforms/twitch#accounts)
  - name: Color
    type: Select
    default: Default
    required: true
    description: |
      Select the color for the announcement

      Options: `Default`, `Blue`, `Green`, `Orange`, `Purple`
  - name: Message
    type: Text
    required: true
    description: |
      Enter the text content for the announcement
csharpMethods:
  - TwitchAnnounce
---

---
title: Set Channel Game
description: Update the current game category of your Twitch channel
parameters:
  - name: Source
    type: Select
    default: String
    description: |
      Select a source type for the new game value

      - `String`: Select this option to manually enter the game title or load it from a variable
      - `Specific Game`: Select this option to select a game from a dropdown
  - name: Title
    type: Text | Select
    description: |
      Select the new game category or enter the new game category by name
variables:
  - name: gameSuccess
    type: bool
    description: The status of the sub-action request
    value: True/False
  - name: gameName
    type: string
    description: The name of the game
    value: Beat Saber
  - name: gameId
    description: The unique game identifier
    value: 503116
  - name: gameBoxArt
    type: string
    description: URL to the cover art image for the selected game
    value:
csharpMethods:
  - SetChannelGame
---

---
title: Effect Success
description: Trigger for a Crowd Control Effect Success
version: 0.2.0
parameters:
  - name: Game
    type: Select
    required: true
    default: Any
    description: Game to which the trigger should react on
  - name: Pack
    type: Select
    required: true
    default: Any
    description: Pack of the game the trigger should react on
  - name: Effect
    type: Select
    required: true
    default: Any
    description: Effect, is based on the Game and Pack
  - name: Type
    type: Select
    required: true
    default: Any
    description:  |
      - `Any`
      - `Immediate`
      - `Timed`
  - name: Price
    type: Range
    description: |
      Filter events between a specified `Min` and `Max`

      `Min` and `Max` are **inclusive** of the entered values

      - `Any Value` - Leave both min and max empty to accept any value
      - `Exact Value` - Enter only a `Max` to trigger on a specific value
      - `Greater Than` - Enter only a `Min` to trigger on any value greater than the specified value
      - `Range` - Enter a min and a max to trigger within a desired range
variables:
  - name: requestID
    type: string
    description: The request id
    value: a2d00d8c-89ef-4f59-aac5-0030a01a53f6
  - name: effect.effectID
    type: string
    description: The id of the effect
    value: removesprite
  - name: effect.type
    type: string
    description: The type of the effect
    value: game
  - name: effect.name
    type: string
    description: The name of the effect
    value: Take Shine Sprite
  - name: effect.duration
    type: number
    description: The duration of the effect
    value: 0
  - name: effect.note
    type: string
    description: The effect note
  - name: effect.category
    type: string
    description: The category of the effect
  - name: effect.description
    type: string
    description: The description of the effect
    value: Steal a shine sprite from the player!
  - name: effect.price
    type: number
    description: The price of the effect
    value: 1
  - name: effect.image
    type: string
    description: The image of the effect
    value: https://resources.crowdcontrol.live/images/PaperMarioTTYD/PaperMarioTTYD/icons/removesprite.png
  - name: price
    type: number
    description: The price
    value: 1
  - name: unitPrice
    type: number
    description: The unit price
    value: 1
  - name: game.gameID
    type: number
    description: The game id
    value: PaperMarioTTYD
  - name: game.name
    type: string
    description: The name of the game
    value: 'Paper Mario: The Thousand-Year Door'
  - name: gamePack.gamePackID
    type: string
    description: The game pack id
    value: PaperMarioTTYD
  - name: gamePack.name
    type: string
    description: The name of the game pack
    value: 'Paper Mario: The Thousand-Year Door'
  - name: gamePack.platform
    type: string
    description: The game pack platform
    value: GCN
  - name: target.ccUID
    type: string
    description: the target ccuuid unique identifier
    value: ccuid-01hb25ab3n9v6861v0855s1wdf
  - name: target.name
    type: string
    description: The target name
    value: Rondhi
  - name: target.profile
    type: string
    description: The target profile
    value: twitch
  - name: target.originID
    type: number
    description: The target origin id
    value: 3405825
  - name: target.image
    type: string
    description: The target image
    value: https://static-cdn.jtvnw.net/jtv_user_pictures/9bb598a0-9fab-4a0c-8ad9-48b41d5ab2fe-profile_image-300x300.png
  - name: requester.ccUID
    type: string
    description: The requester ccuid unique id
    value: ccuid-01hkkmd53tdf7q4bf43k58effq
  - name: requester.name
    type: string
    description: The requester name
    value: KermitThePOGGIES
  - name: requester.profile
    type: string
    description: The requester profile
    value: twitch
  - name: requester.originID
    type: number
    description: the requester origin id
    value: 738066902
  - name: requester.image
    type: string
    description: The requester image
    value: https://static-cdn.jtvnw.net/jtv_user_pictures/4ad22e7e-ac1d-404d-b820-cab16d16f98f-profile_image-300x300.png
  - name: timestamp
    type: number
    description: The timestamp of the event
    value: 1704830667420
---
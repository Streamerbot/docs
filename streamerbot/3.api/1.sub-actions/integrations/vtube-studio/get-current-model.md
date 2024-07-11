---
title: Get Current Model
description: Get info about the currently loaded model
variables:
  - name: model.id
    type: string
    description: The ID of the model
    value: 62c6a71a4d324204afd25f61445f8e4f
  - name: model.name
    type: string
    description: The name of the model
    value: hijiki
  - name: model.vtsModelName
    type: string
    description: The vts name of the model
    value: hijiki.vtube.json
  - name: model.vtsModelIconName
    type: string
    description: The vts name of the model icon
    value: icon.jpg
  - name: model.live2DModelName
    type: string
    description: The live 2d model name
    value: hijiki.model3.json
  - name: model.loadTime
    type: int
    description: Time in milliseconds it took to load the current model
    value: 1680
  - name: model.timeSinceLoaded
    type: int
    description: Contains the time in milliseconds since the model has been loaded
    value: 419903
  - name: model.numberOfLive2DParameters
    type: int
    description: Number of live 2d parameters
    value: 29
  - name: model.numberOfLive2DArtmeshes
    type: int
    description: Number of live 2d art meshes
    value: 136
  - name: model.hasPhysicsFile
    type: bool
    description: Flag whether the model has a physics file
    value: True/False
  - name: model.numberOfTextures
    type: int
    description: Number of textures
    value: 1
  - name: model.textureResolution
    type: int
    description: The models' texture resolution
    value: 1024
  - name: model.posX
    type: double
    description: X position of the model
    value: -0.132193565368652
  - name: model.posY
    type: double
    description: Y position of the model
    value: -0.162023842334747
  - name: model.rotation
    type: double
    description: Rotation of the model
    value: 9.33
  - name: model.size
    type: double
    description: Size of the model
    value: 57.6690902709961
csharpMethods:
  - VTubeStudioGetModelPosition
---

---
title: Send Raw Request
description: Send a raw request to VTube Studio
parameters:
  - name: Name
    type: String
    required: false
    description: Name of the raw request (optional)
  - name: Variable Prefix
    type: String
    required: true
    description: Prefix of the populated variables, `vtsRaw` by default. For example `vtsRaw.data.modelName`
  - name: Request
    type: String
    required: true
    description: Exact name of the request
  - name: JSON
    type: JSON
    required: true
    description: The JSON request
variables:
  - name: warnedUser
    type: string
    description: display name of the warned user
    value: PewDiePie
csharpMethods:
  - VTubeStudioSendRawRequest
---

## Example
Here's an example of a `CurrentModelRequest` to get information about the current model:

![VTS Raw Example Request](assets/vts-raw-example-1.png)

Running the action will then populate these variables:

![VTS Raw Example Response](assets/vts-raw-example-2.png)

For all requests, please refer to the VTS documentation: https://github.com/DenchiSoft/VTubeStudio?tab=readme-ov-file#api-details

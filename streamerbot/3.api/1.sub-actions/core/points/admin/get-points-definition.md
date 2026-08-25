---
title: Get Points Definition
description: Fetch the current points definition for a specific point
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to fetch
  - name: Destination Variable
    type: string
    description: The variable to store the fetched points definition
csharpMethods:
  - GetPointDefinition
  - GetPointDefinitions
---
---
title: Set Channel Category
description: Update the current category of your Kick channel
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
  - name: category.success
    type: bool
    description: The status of the sub-action request
    value: True/False
  - name: category.id
    type: string
    description: The unique category identifier
    value: 5787
  - name: category.name
    description: The unique category name
    value: Cats & Soup
  - name: category.thumbnail
    type: string
    description: URL to the image for the selected category
    value: https://files.kick.com/images/subcategories/5787/banner/conversion/153f16f9-6a5a-4449-b7c2-0a8e14f18092-banner.webp
csharpMethods:
  - KickSetCategory
---
---
title: Channel Update
description: Trigger for a Kick Channel Update
variables:
  - name: categoryUpdated
    type: bool
    description: Whether or not the category been updated
    value: True
  - name: categoryId
    type: string
    description: The unique category identifier
    value: 5787
  - name: categoryName
    description: The unique category name
    value: Cats & Soup
  - name: categoryThumbnail
    type: string
    description: URL to the image for the selected category
    value: https://files.kick.com/images/subcategories/5787/banner/conversion/153f16f9-6a5a-4449-b7c2-0a8e14f18092-banner.webp
  - name: oldCategoryId
    type: string
    description: The old category identifier
    value: 5787
  - name: oldCategoryName
    description: The old category name
    value: Cats & Soup
  - name: oldCategoryThumbnail
    type: string
    description: URL to the image for the old category
    value: https://files.kick.com/images/subcategories/5787/banner/conversion/153f16f9-6a5a-4449-b7c2-0a8e14f18092-banner.webp
  - name: statusUpdated
    type: bool
    description: Whether or not the stream title was updated
    value: True
  - name: status
    description: The current stream title
    value: My stream title
  - name: oldStatus
    description: The old stream title
    value: My old stream title
commonVariables:
  - KickBroadcaster
  - KickUser
---

## Details
This triggers when the title or the description changes on your stream.

## Parameters
::field-group
  ::field{name="Game Only" type=Checkbox}
    Check this field if you only want this to trigger when the game changes
  ::
  ::field{name=Game type=Select}
    Select a game if you only want this to trigger when the stream changes to this game
  ::
::

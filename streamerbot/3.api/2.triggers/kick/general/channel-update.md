---
title: Channel Update
description: Trigger for a Kick Channel Update
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
commonVariables:
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

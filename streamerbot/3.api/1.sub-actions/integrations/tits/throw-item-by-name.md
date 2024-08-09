---
title: Throw Item by Name
description: Allows for throwing a specific item by name
version: 0.2.3
parameters:
  - name: Item
    type: String
    required: true
    description: Type the item name you wish to throw into the input box
  - name: Delay
    type: Double
    required: true
    description: Type the delay between throws (in 0.1 second increments)
  - name: Amount
    type: Int
    required: true
    description: Select the number of the selected items to be thrown
csharpMethods:
  - ThrowingSystemThrowItemByName
---

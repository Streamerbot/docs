---
title: Get Random Number
description: Generate a random number for usage in subsequent sub-actions
parameters:
  - name: Type
    type: Select
    default: Between
    description: |
      - `Between`: Generate a random `int`{lang=cs} between configured min/max values, inclusive
      - `Next Float`: Select a random `float`{lang=cs} value between `0` and `1`
  - name: Between
    type: Range
    description: If `Type` is `Between`, you can use this setting to configure the min/max values
variables:
  - name: randomNumber
    type: int
    description: If `Between` is selected, an integer value between your configured min and max, inclusive
    value: 10
  - name: randomFloat
    type: float
    description: If `Next Float` is selected, a floating point value between 0 and 1
    value: 0.23
  - name: randomPercent
    type: int
    description: If `Next Float` is selected, the `randomFloat` value represented as a percentage
    value: 23
csharpMethods:
  - Between
  - NextDouble
---

---
name: Range
type: Select
description: |
  Filter events between a specified `Min` and `Max`

  ::note
    `Min` and `Max` are **inclusive** of the entered values
  ::
options:
  - value: Any Value
    description: Trigger on any value by leaving both `Min` and `Max` empty
  - value: Exact Value
    description: Trigger on an exact value by specifying only a `Max` value
  - value: Greater Than
    description: Trigger on values greater than or equal to a value by specifying only a `Min` value
  - value: Range
    description: Trigger on values within the specified range by specifying both a `Min` and `Max`
---
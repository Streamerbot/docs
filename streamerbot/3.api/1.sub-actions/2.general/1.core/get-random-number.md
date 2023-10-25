# Get Random Number
Generate a random number for usage in subsequent sub-actions
:image-preview

## Parameters
### `Type`
- `Between`: Select a random number between configured min/max values
- `Next Float`: Select a random float value between `0` and `1`

### `Between`
Configure your preferred min/max values

## Variables
:variables-description

Name | Description | Example
----:|:------------|---------|
`randomNumber` | If `Between` is selected, an integer value between your configured min/max | `23`
`randomFloat` | If `Next Float` is selected, a floating point value between 0 and 1 | `0.23`
`randomPercent` | If `Next Float` is selected, the `randomFloat` value represented as a percentage | `23`

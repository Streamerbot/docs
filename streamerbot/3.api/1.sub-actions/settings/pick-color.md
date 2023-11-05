---
title: Pick Color
description: Select a color and populate a set of variables
---

Convert a selected color into a bank of variables that can then be passed to C# code, HTML objects, or any OBS source that is color-aware.

## Parameters
### `Color / OBS Color`
The Color picker will give the standard pallet picker so you can chose by a slider or by entering raw RGB / HSL values

Once a color is chosen the `Color` box will be populated with the RGB Hex value and `OBS Color` will populate with the raw integer value OBS expects for ABGR it uses for its natively supported sources.

### `Variable Name`
Enter an alias for the resulting variables, outlined below. Don't use %'s in this field this will be done automatically.

## Variables
:variables-description


Name | Description
----:|:------------
`variableName.color.a` | The alpha value
`variableName.color.r` | The red value
`variableName.color.g` | The green value
`variableName.color.b` | The blue value
`variableName.html` | The html color code
`variableName.htmlalpha` | The html color code with alpha value
`variableName.obs` | The color as an OBS ABGR value

::callout{icon=i-mdi-alert color=amber}
Replace `variableName` with the variable name you configured.
::
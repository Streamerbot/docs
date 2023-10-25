---
version: 0.0.50
---

# Prediction Updated
This triggers when a prediction gets updated.

## Details
::list
- Twitch Service: `EventSub`
::

## Variables
:variables-description
Name | Description
----:|:------------
`prediction.Id` | Twitch's id of the prediction
`prediction.CreatedAt` | The timestamp that the prediction was created
`prediction.Title` | The title of the prediction
`prediction.PredictionWindow` | How many seconds the prediction last
`prediction.outcome#.id` | The id for this outcome
`prediction.outcome#.title` | The title for this outcome
`prediction.outcome#.users` | How many users voted for this outcome
`prediction.outcome#.points` | The total channel points used for this outcome
`prediction.outcome#.color` | In caps the color name for this outcome e.g. `BLUE` or `PINK`
`prediction._json` | All the variables in a JSON Object

::callout{color=amber icon=i-mdi-lightbulb}
Change the `#` incrementing from 0. So e.g. `variable0%` `variable1%` `variable2%`
::
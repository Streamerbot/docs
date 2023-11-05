---
version: 0.0.50
---

# Prediction Completed
This triggers when a prediction gets completed.

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
`prediction.LockedAt` | The timestamp that the prediction was locked
`prediction.EndedAt` | The timestamp that the prediction ended
`prediction.winningOutcome.id` | The id of the winning outcome
`prediction.winningOutcome.title` | The title of the winning outcome
`prediction.winningOutcome.users` | The votes for the winning outcome
`prediction.winningOutcome.points` | The count of channel points used for the winning outcome
`prediction.winningOutcome.color`	| In caps the color name e.g. `BLUE` or `PINK`
`prediction._json` | All the variables in a JSON Object

::callout{color=amber icon=i-mdi-lightbulb}
> Change the `#` incrementing from 0. So e.g. `variable0%` `variable1%` `variable2%`
::
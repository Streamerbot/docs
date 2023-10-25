---
title: Predictions
description: Twitch Events Reference
published: true
date: 2023-04-08T20:20:26.136Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:38.706Z
---

## Variables
> With `prediction.outcome#` you need to change the `#` from 0 to 9
{.is-info}

### Prediction Created
Name | Description
----:|:------------
`prediction.Id` | Twitch's ID of the prediction
`prediction.CreatedAt` | When it was created
`prediction.Title` | It's title
`prediction.PredictionWindow` | the duration of the prediction, in seconds
`prediction.outcome#.id` | Title for this outcome
`prediction.outcome#.title` | Win
`prediction.outcome#.users` | How many users picked this outcome
`prediction.outcome#.points` | Total number of rewards used
`prediction.outcome#.color` | In caps the color name e.g. `BLUE` or `PINK`
`prediction._json` | All the variables in a JSON Object

### Prediction Updated
Name | Description
----:|:------------
`prediction.Id` | Twitch's ID of the prediction
`prediction.CreatedAt` | When it was created
`prediction.Title` | It's title
`prediction.PredictionWindow` | the duration of the prediction, in seconds
`prediction.outcome#.id` | Title for this outcome
`prediction.outcome#.title` | Win
`prediction.outcome#.users` | How many users picked this outcome
`prediction.outcome#.points` | Total number of rewards used
`prediction.outcome#.color` | In caps the color name e.g. `BLUE` or `PINK`
`prediction._json` | All the variables in a JSON Object

### Prediction Locked
Name | Description
----:|:------------
`prediction.Id` | Twitch's ID of the prediction
`prediction.CreatedAt` | When it was created
`prediction.Title` | It's title
`prediction.PredictionWindow` | the duration of the prediction, in seconds
`prediction.outcome#.id` | Title for this outcome
`prediction.outcome#.title` | Win
`prediction.outcome#.users` | How many users picked this outcome
`prediction.outcome#.points` | Total number of rewards used
`prediction.outcome#.color` | In caps the color name e.g. `BLUE` or `PINK`
`prediction.LockedAt` | When it was locked
`prediction.EndedAt` | When it ended

### Prediction Resolved
Name | Description
----:|:------------
`prediction.Id` | Twitch's ID of the prediction
`prediction.CreatedAt` | When it was created
`prediction.Title` | It's title
`prediction.PredictionWindow` | the duration of the prediction, in seconds
`prediction.outcome#.id` | Title for this outcome
`prediction.outcome#.title` | Win
`prediction.outcome#.users` | How many users picked this outcome
`prediction.outcome#.points` | Total number of rewards used
`prediction.outcome#.color` | In caps the color name e.g. `BLUE` or `PINK`
`prediction.LockedAt` | When it was locked
`prediction.EndedAt` | When it ended
`prediction.winningOutcome.id` | The ID of the winning outcome
`prediction.winningOutcome.title` | The title of the winning outcome
`prediction.winningOutcome.users` | How many users voted for this prediction
`prediction.winningOutcome.points` | The total number of channel points used by users
`prediction.winningOutcome.color`	| In caps the color name e.g. `BLUE` or `PINK`
`prediction._json` | All the variables in a JSON Object

### Prediction Canceled
Name | Description
----:|:------------
`prediction.Id` | Twitch's ID of the prediction
`prediction.CreatedAt` | When it was created
`prediction.Title` | It's title
`prediction.PredictionWindow` | the duration of the prediction, in seconds
`prediction.outcome#.id` | Title for this outcome
`prediction.outcome#.title` | Win
`prediction.outcome#.users` | How many users picked this outcome
`prediction.outcome#.points` | Total number of rewards used
`prediction.outcome#.color` | In caps the color name e.g. `BLUE` or `PINK`
`prediction.LockedAt` | When it was locked
`prediction.EndedAt` | When it ended

The above are available for all prediction events

Because how some of this is handled, it is recommended that Execute C# code is used for these as some logic maybe required

**Note** if there are variables missing that you think maybe of benefit, let us know [here](https://ideas.streamer.bot) and we can likely add them in

## Basic Creation Example
To create a prediction outside of the UI, you will need to use [Execute C# Code](/Sub-Actions/Code/CSharp), a simple example is provided below.  I've added a few comments to it which hopefully will help you get it setup for your usage.  If you still have questions, be sure to ask them in the discord!

### Code

```csharp
using System;
using System.Collections.Generic;

public class CPHInline
{
	public bool Execute()
	{
		// replace the text between the "'s with the prediction title
		var predictionTitle = "Which prediction option is best?";

    // these are your prediction options, you can have upto 10, if you don't want 10, just delete the lines you don't want, so say
    // you would like 2, delete Option 3, 4, 5, 6, 7, 8, 9 and 10
    // and be sure to rename your options by changing the text inbetween the "'s
    var predictionOptions = new List<string>();
    predictionOptions.Add("Option 1");
    predictionOptions.Add("Option 2");
    predictionOptions.Add("Option 3");
    predictionOptions.Add("Option 4");
    predictionOptions.Add("Option 5");
    predictionOptions.Add("Option 6");
    predictionOptions.Add("Option 7");
    predictionOptions.Add("Option 8");
    predictionOptions.Add("Option 9");
    predictionOptions.Add("Option 10");

    // change the number below to alter the duration of the prediction, it is in seconds
    var duration = 60;

    CPH.TwitchPredictionCreate(predictionTitle, predictionOptions, duration);

		return true;
	}
}
```

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}
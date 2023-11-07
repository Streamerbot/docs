---
title: Polls
description: Twitch Events Reference
published: true
date: 2023-04-08T20:20:23.852Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:34.620Z
---

## Twitch Polls
With Twitch polls, you can drive interactive elements on your stream, showing your viewers choices in real time!  You could also create polls when certain actions happen, or setup some pre-defined polls, and just assign the actions to keys on your StreamDeck (or TouchPortal) for quick and easy access!

The usage of Polls within Streamer.bot can be a bit more complex, so be sure to ask in the Discord if you get stuck!

**Note** I do plan on adding a `Sub-Action` for creating polls, at least, it's on my list, so this will provide another path, other then the [C# Example](#basic-creation-example) shown below.

## Variables
> With `poll.choice#` you need to change the `#` from 0 to 4
{.is-info}

### Created
Name | Description
----:|:------------
`poll.Id` | Twitch's ID for the poll
`poll.StartedAt` | The time that the poll stared <br> `d/M/yyyy HH:mm:ss`
`poll.Title` | The title of the poll
`poll.Duration` | How long the poll will run for, in seconds
`poll.DurationRemaining` | How much longer the poll has left, in seconds
`poll.choices.count` | The number of choices
`poll.choice#.title` | The title of the poll choice
`poll.choice#.votes` | Number of regular votes for the choice
`poll.choice#.bitVotes` | Number of bit based votes for the choice
`poll.choice#.rewardVotes` | Total number of reward based votes
`poll.choice#.totalVotes` | Total number of votes for the choice
`poll.votes` | Total number of regular votes
`poll.bitVotes` | Total number of bit based votes
`poll.rewardVotes` | Total number of reward based votes
`poll.totalVotes` | Overall total number of votes
`poll._json` | All the variables in a JSON Object
{.vars-table}

### Updated
Name | Description
----:|:------------
`poll.Id` | Twitch's ID for the poll
`poll.StartedAt` | The time that the poll stared <br> `d/M/yyyy HH:mm:ss`
`poll.Title` | The title of the poll
`poll.Duration` | How long the poll will run for, in seconds
`poll.DurationRemaining` | How much longer the poll has left, in seconds
`poll.choices.count` | The number of choices
`poll.choice#.title` | The title of the poll choice
`poll.choice#.votes` | Number of regular votes for the choice
`poll.choice#.bitVotes` | Number of bit based votes for the choice
`poll.choice#.rewardVotes` | Total number of reward based votes
`poll.choice#.totalVotes` | Total number of votes for the choice
`poll.votes` | Total number of regular votes
`poll.bitVotes` | Total number of bit based votes
`poll.rewardVotes` | Total number of reward based votes
`poll.totalVotes` | Overall total number of votes
`poll._json` | All the variables in a JSON Object
{.vars-table}

### Completed
Name | Description
----:|:------------
`poll.Id` | Twitch's ID for the poll
`poll.StartedAt` | The time that the poll stared <br> `d/M/yyyy HH:mm:ss`
`poll.Title` | The title of the poll
`poll.Duration` | How long the poll will run for, in seconds
`poll.DurationRemaining` | How much longer the poll has left, in seconds
`poll.choices.count` | The number of choices
`poll.choice#.title` | The title of the poll choice
`poll.choice#.votes` | Number of regular votes for the choice
`poll.choice#.bitVotes` | Number of bit based votes for the choice
`poll.choice#.rewardVotes` | Total number of reward based votes
`poll.choice#.totalVotes` | Total number of votes for the choice
`poll.votes` | Total number of regular votes
`poll.bitVotes` | Total number of bit based votes
`poll.rewardVotes` | Total number of reward based votes
`poll.totalVotes` | Overall total number of votes
`poll.EndedAt` | The time that the poll ended <br> `d/M/yyyy HH:mm:ss`
`poll.winningIndex` | The index of the winning choice, from 0 to 4
`poll.winningChoice.id` | The ID of the winning choice
`poll.winningChoice.title` | The title of the winning choice
`poll.winningChoice.votes` | Number of regular votes
`poll.winningChoice.bitVotes` | Number of bit based votes
`poll.winningChoice.rewardVotes` | Number of channel point based votes
`poll.winningChoice.totalVotes` | Total number of votes for the choice
`poll._json` | All the variables in a JSON Object
{.vars-table}

### Terminated

Name | Description
----:|:------------
`poll.Id` | Twitch's ID for the poll
`poll.StartedAt` | The time that the poll stared <br> `d/M/yyyy HH:mm:ss`
`poll.Title` | The title of the poll
`poll.Duration` | How long the poll will run for, in seconds
`poll.DurationRemaining` | How much longer the poll has left, in seconds 
`poll.choices.count` | The number of choices
`poll.choice#.title` | The title of the poll choice
`poll.choice#.votes` | Number of regular votes for the choice
`poll.choice#.bitVotes` | Number of bit based votes for the choice
`poll.choice#.rewardVotes` | Total number of reward based votes
`poll.choice#.totalVotes` | Total number of votes for the choice
`poll.votes` | Total number of regular votes
`poll.bitVotes` | Total number of bit based votes
`poll.rewardVotes` | Total number of reward based votes
`poll.totalVotes` | Overall total number of votes
`poll.EndedAt` | The time that the poll ended <br> `d/M/yyyy HH:mm:ss`
`poll.winningIndex` | The index of the winning choice, from 0 to 4
`poll.winningChoice.id` | The ID of the winning choice
`poll.winningChoice.title` | The title of the winning choice
`poll.winningChoice.votes` | Number of regular votes
`poll.winningChoice.bitVotes` | Number of bit based votes
`poll.winningChoice.rewardVotes` | Number of channel point based votes
`poll.winningChoice.totalVotes` | Total number of votes for the choice
`poll._json` | All the variables in a JSON Object
{.vars-table}

Because how some of this is handled, it is recommended that Execute C# code is used for these as some logic maybe required

**Note** if there are variables missing that you think maybe of benefit, let me know and I can likely add them in

## Basic Creation Example

Since the initial usage of creating polls currently requires [Execute C# Code](/Sub-Actions/Code/CSharp), a simple example is provided below.  I've added a few comments to it which hopefully will help you get it setup for your usage.  If you still have questions, be sure to ask them in the discord!

### Code

```csharp
using System;
using System.Collections.Generic;

public class CPHInline
{
	public bool Execute()
	{
		// replace the text between the "" with the poll question
		string pollQuestion = "Which poll option is best?";

		// these are your poll options, you can have upto 5, if you don't want 5, just delete the lines you don't want, so say
		// you would like 2, delete Option 3, 4, and 5.
		// and be sure to rename your options by changing the text inbetween the ""
		List <string> pollOptions = new List<string>();
		pollOptions.Add("Option 1");
		pollOptions.Add("Option 2");
		pollOptions.Add("Option 3");
		pollOptions.Add("Option 4");
		pollOptions.Add("Option 5");

		// change the number below to alter the duration of the poll, it is in seconds
		int duration = 60;

		// the next option, leave it at 0 to disable them, or, set it to a value to enable them
		int channelPointsPerVote = 0;

		CPH.TwitchPollCreate(pollQuestion, pollOptions, duration, channelPointsPerVote);

		return true;
	}
}
```

### Import String

For easier importing, here is an import string you can use, right click in `Actions`, and choose `Import`

```
TlM0RR+LCAAAAAAABAClVk2TokgQvW/E/gejr7vdi4DTMjfBBrFtd6RHENY5UFQ1IsXH8CHgxPz3TQqdRt05TKwRBFKZ9fJlvkyob7//NhjcHUiWB0l893HA/8kWYjci8HSnZMQtyOBTQungqXajlJK7zsP1CtiRg9M/7fNg8K27gSnA7VY0dkePooTuxbEg3YtvmNyPXVG4J56EsOiJwnAodlhs09eSlG3IuKT0fZXELqKkxSuykvTWa4+WmKhZEs2CvEiyBlzeXJr3fC5zaFPohfOzpExba7ue9wwurdwmN8r4FjBzY5xEE5b4rdVLYq/MMhIXt7abYl0U7D/YdhVXEkzeqTE3THIvC9IThbsra0hIOqHBgdxQ6BIgbwQIeuSKCTMqH7dbK4AMq3y7fQm8LMmTt+Jh+fR5u1UzYFclWfhB3G4P4gP3IHDCUNpuo9xLMhqgB9yv7v9BfG3ygkQMrw/35TIT1BSEVQdqgDfLFEWevxboEWtm8XfFPV+vLcLlAWk1tQUjRfzouAgxRZHZuNbL43SVLJVYHtpRndqNvEeaevQaebp+2s0RrKFoDfZ8qQQTX1fkClvzHPb5diQdkCKrRDP3eGPQZyU8+7SYcJ+crvFBn82pp9U7m1/7WNtRfWZQMlsBhslh3qQokDlXW/t6oPuYp5yrdM+eJuUQo8aWCXnQA/K553dc+Yhnc5Yn81PVobNZcq4llfqU83WKE9daJvpMhtwrHwlyZ9PoUdeAj7D6S99DXheYk8OiaWObR+dV3nnR2ieWNPQCuUJ8neuaVDEe8Uuuz+gBv8p72xJ9V1N58B96M+OgT9fgR6OTPUS8GGNFFmxrxHW2dAixfUczcwfqBrVIYC/UdESh7iMkrMEmlXPwwbxaYqXyPX4Mlzq6rSuLISABsJQWo6D6VIcYBkWayQHuJ+AEmov+S1P5S8ACHiHwKG+wNLUEjAD2HPFm3vJiuqFILWANeJlNL3/fjkPf5nc7FGGmQV9XyCWA3ATHMssuvwkoe6Hdiwta6dP6rOEfnU71ie/o2GoIPSroT3UK9Rp7ggH9Ooo/BX7a9ngPi2nz+aSv14xkR1slenjiGkxqPQgve/Iq1iJUQ0fxgzMG1DB4/nzu+e5iPfb0I/9yZRnhszLv1Vf/VV7cr/Nad7xue3bvtvqd50sbDZEFPR6AnlZ9wNDTqJF3CPTxTrPmzMzG3nTcEW+f9GOz0vYv180JBf2W1Oal0pm9XNTDbftZM4ZepP6YueV+0r1Pen6LZnzmxHrjPIcL6FfHYnOTwnzssDKpWM9pRgq9HiCtywW9trMLPQ08wK/1ZbnoMwfyMbs+1czShvcSYLWzW1zUFHKAPaw+0E/5WpNSFBvHtWY2ZiTBjEwkfXrLezWU9QU1BHdj7F2V6TL1InOHtXVy/b5Z3Ghd9esL9VwmMHclaLFCPPCZLVfOZm4hAd6bN3rKDcwO1FX0YTaGzo8+lKXpKpWuvnlpRrwkSgP6k48eJtRtXgs3u/0uM3t3WuHHEidxBA4qwgiOLB8ex/foDeH7N08SPIQeyYgIV4ErEvi7FpR74C4tRZO2ZKT2d2k5HzsuTjnM8pOTTkcxxqRuA72vfj///XJ9ytDaEOwD/6V/OKHUTXOCe9bOyIA6z+4M1tsK26IIDj1n/+//AhCOG/MuCgAA
```

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}
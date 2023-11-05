---
title: Update
description: Channel Point Rewards Sub-Actions Reference
published: true
date: 2023-02-04T12:10:55.989Z
tags: twitch, channel-points, subactions
editor: markdown
dateCreated: 2022-06-11T05:05:44.509Z
---

## Overview
Modify the `Title`, `Prompt` and `Cost` of a channel point reward at once.

![overview.png](/Sub-Actions/Twitch/update/overview.png =400x)

## Configuration
### `Reward`
Select the reward.

- Type: `Selection`

### Title
Enter the new title for your channel point reward.

### Prompt
Enter the text to apply to your reward prompt.

### Cost
Enter the amount you would like to set or modify

### Operator
Name | Description
----:|:------------
`None` | Set the cost to the amount entered
`Add` | Add the amount entered to the current cost
`Subtract` | Subtract the amount entered from the current cost
`Multiply` | Multiplay the amount entered with the current cost
`Divide` | Divice the current cost by the amount entered

### Reset to Original
Revert all reward settings to their original values.

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}
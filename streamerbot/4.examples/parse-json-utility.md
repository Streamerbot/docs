---
title: Parse JSON Utility
description: Example code for parsing arbitrary JSON data into Streamer.bot variables
icon: vscode-icons:file-type-json
author: Whipstickgostop
difficulty: 1
---

Sometimes you may want to parse JSON data from an API response or other source into Streamer.bot variables for use in your actions. This utility action provides a simple way to do that using C# code.

This utility action will take a JSON string as input, parse it, and store the resulting data in Streamer.bot variables that you can use in subsequent actions.

:streamerbot-import-card{name="[Utilities] Parse JSON" author="Whipstickgostop" expanded}

## Setup

::steps{level=3}

### Load the import code

1. Copy the import code above
1. Click **Import** at the top of Streamer.bot to open the Import Dialog
1. Paste the import code into the **Import String** field in Streamer.bot

### Confirm the Import

You should see the **Name** field populated with `[Utilities] Parse JSON` with a single action.

Click **Import** to add the Parse JSON Utility to your Streamer.bot instance.

::success
All selected actions will be added to your Streamer.bot installation!
::

::

## Usage

::steps{level=3}

### Prepare your action

- Create a new action, or open an existing action where you would like to parse JSON data.
- Populate an argument named `json` with the JSON string you wish to parse. This can be from a previous action, API response, or any other source.
- The [Set Argument](/api/sub-actions/core/arguments/set-argument) sub-action may be useful for this.

### Run the Parse JSON utility

- Add the [Execute C# Method](/api/sub-actions/core/csharp/execute-csharp-method) sub-action to your action. Ensure it is _after_ you have set the `json` argument.
- Select the `[Utilities] Parse JSON` code, and the `Execute` method.
- Click `OK` to confirm.

### Access the parsed data

After running the Parse JSON utility, the parsed data will be available in Streamer.bot variables.

For example, if your JSON data looks like this...

```json
{
  "user": {
    "name": "StreamerBot",
    "age": 5,
    "isActive": true
  },
  "stats": {
    "followers": 1000,
    "views": 50000
  },
  "status": "ok"
}
```

You can then access the data using the following variable names in any subsequent sub-actions:

| JSON Path         | Variable Name                     |
| ----------------- | --------------------------------- |
| `user.name`       | `%json.user.name%`{lang=cs}       |
| `user.age`        | `%json.user.age%`{lang=cs}        |
| `user.isActive`   | `%json.user.isActive%`{lang=cs}   |
| `stats.followers` | `%json.stats.followers%`{lang=cs} |
| `stats.views`     | `%json.stats.views%`{lang=cs}     |
| `status`          | `%json.status%`{lang=cs}          |

::

---
title: Parse JSON Utility
description: Example code for parsing arbitrary JSON data into Streamer.bot variables
icon: vscode-icons:file-type-json
navigation: false
author: Whipstickgostop
difficulty: 1
---

Sometimes you may want to parse JSON data from an API response or other source into Streamer.bot variables for use in your actions. This utility action provides a simple way to do that using C# code.

This utility action will take a JSON string as input, parse it, and store the resulting data in Streamer.bot variables that you can use in subsequent actions.

## Setup

::steps{level=3}

### Load the import code

- Click **Import** at the top of Streamer.bot to open the Import Dialog
- Paste the following code into the **Import String** field:

:streamerbot-import{code="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"}

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

---
title: DoAction
description: Trigger an action in Streamer.bot via HTTP
navigation.title: DoAction
navigation.icon: tabler:http-post
---

## Request

::field{name="/DoAction" type=POST}

Request body `application/json`{.text-muted}

::code-group
  ```json [Body]
  // Content-Type: application/json
  {
    "action": {
      "id": "<guid>",
      "name": "<name>"
    },
    "args": {
      "key": "value"
    }
  }
  ```
  ```json [Execute by ID]
  // Execute action by ID
  {
    "action": { "id": "4af4bdef-f396-521f-a1a5-02983ae638cb"}
  }
  ```
  ```json [Execute by Name]
  // Execute action by name
  {
    "action": { "name": "My Action" }
  }
  ```
::

::

### Parameters
::field-group
  ::field{name="action" type=object required=true}
  The Streamer.bot action to trigger, identified by its GUID or name.
  ::
  ::field{name="args" type="Dictionary<string, object>"}
  Optional arguments to pass to the action as key-value pairs.
  ::
::

## Response

`204 No Content`{color=success}

## Example

::code-group
  ```bash [Terminal]
  curl -X POST http://127.0.0.1:7474/DoAction \
    -H "Content-Type: application/json" \
    -d '{
      "action": {
        "id": "your-action-guid",
        "name": "Your Action Name"
      },
      "args": {
        "customArg": "customValue"
      }
    }'
  ```

  ```js [js]
  const response = await fetch('http://127.0.0.1:7474/DoAction', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({
      action: {
        id: 'your-action-guid',
        name: 'Your Action Name'
      },
      args: {
        customArg: 'customValue'
      }
    })
  });
  console.log(response.status); // 204
  ```

  ```py [py]
  import requests
  import json

  data = {
    "action": {
      "id": "your-action-guid",
      "name": "Your Action Name"
    },
    "args": {
      "customArg": "customValue"
    }
  }

  response = requests.post(
    'http://127.0.0.1:7474/DoAction',
    headers={'Content-Type': 'application/json'},
    data=json.dumps(data)
  )
  print(response.status_code)  # 204
  ```
::
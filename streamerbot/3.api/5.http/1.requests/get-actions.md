---
title: GetActions
description: Retrieve the list of actions via HTTP in Streamer.bot
navigation.title: GetActions
navigation.icon: tabler:http-get
---

### Request

::field{name="/GetActions" type=GET}
No parameters
::

### Response

```json
{
  "actions": [
    {
      "id": "<action guid>",
      "name": "<action name>"
    }
  ]
}
```

### Example

::code-group
  ```bash [Terminal]
  curl -X GET http://127.0.0.1:7474/GetActions
  ```

  ```js [js]
  const response = await fetch('http://127.0.0.1:7474/GetActions');
  const data = await response.json();
  console.log(data);
  ```

  ```py [py]
  import requests
  response = requests.get('http://127.0.0.1:7474/GetActions')
  data = response.json()
  print(data)
  ```
::

---
title: ClearCredits
description: Clear the credits via HTTP in Streamer.bot
navigation.title: ClearCredits
navigation.icon: tabler:http-get
---

### Request

::field{name="/ClearCredits" type=GET}
No parameters
::

### Response

`204 No Content`{color=success}

### Example

::code-group
  ```bash [Terminal]
  curl -X GET http://127.0.0.1:7474/ClearCredits
  ```

  ```js [js]
  const response = await fetch('http://127.0.0.1:7474/ClearCredits', {
    method: 'GET'
  });
  console.log(response.status); // 204
  ```

  ```py [py]
  import requests
  response = requests.get('http://127.0.0.1:7474/ClearCredits')
  print(response.status_code)  # 204
  ```
::
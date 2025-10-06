---
title: GetCredits
description: Retrieve the current credits data via HTTP in Streamer.bot
navigation.title: GetCredits
navigation.icon: tabler:http-get
---

### Request

::field{name="/GetCredits" type=GET}
No parameters
::

### Response

```json
{
  "Events": {
    "Follows": [],
    "Cheers": [],
    "Subs": [],
    "ReSubs": [],
    "GiftSubs": [],
    "GiftBombs": [],
    "Raided": [],
    "RewardRedemptions": [],
    "GoalContributions": [],
    "GameUpdates": [],
    "Pyramids": []
  },
  "HypeTrainConductor": [],
  "HypeTrainContributors": [],
  "User": {
    "Editors": [],
    "Moderator": [],
    "Subscriber": [],
    "VIPs": [],
    "Users": [],
    "regulars": []
  },
  "Custom": {},
  "TopBits": {
    "All": [],
    "Month": [],
    "Week": []
  },
  "TopChannelRewards": []
}
```

### Example

::code-group
  ```bash [Terminal]
  curl -X GET http://127.0.0.1:7474/GetCredits
  ```

  ```js [js]
  const response = await fetch('http://127.0.0.1:7474');
  const data = await response.json();
  console.log(data);
  ```

  ```py [py]
  import requests
  response = requests.get('http://127.0.0.1:7474')
  data = response.json()
  print(data)
  ```
::
---
title: TestCredits
description: Test the credits data via HTTP in Streamer.bot
navigation.title: TestCredits
navigation.icon: tabler:http-get
---

### Request

::field{name="/TestCredits" type=GET}
No parameters
::

### Response

Returns the same structure as `/GetCredits` but with dummy data filled in for testing purposes.

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
  curl -X GET http://127.0.0.1:7474/TestCredits
  ```

  ```js [js]
  const response = await fetch('http://127.0.0.1:7474/TestCredits');
  const data = await response.json();
  console.log(data);
  ```

  ```py [py]
  import requests
  response = requests.get('http://127.0.0.1:7474/TestCredits')
  data = response.json()
  print(data)
  ```
::
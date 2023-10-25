# Raw
### Tabs {.tabset}
#### Action
```json
{
  "id": "cc8a2cd1-eb33-45b0-9f16-f752abe6fbff",
  "name": "PyramidSuccess",
  "arguments": {
    "totalPyramids": 4,
    "pyramidWidth": 3,
    "pyramidEmote": "nate121Heart"
  },
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": true,
    "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
  }
}
```

#### SubAction
```json
{
  "parentId": "cc8a2cd1-eb33-45b0-9f16-f752abe6fbff",
  "parentName": "PyramidSuccess",
  "type": 10,
  "id": "29e34a9b-5856-4133-85eb-f812597c4d89",
  "name": "Message (Nice %pyramidWidth%-width %pyramidEmote%…)",
  "arguments": { /* arguments can and will vary depending on the type of subaction */
    "totalPyramids": 4,
    "pyramidWidth": 3,
    "pyramidEmote": "nate121Heart",
    "user": "<user's display name>", /* user who triggered action */
    "userName": "<username>", /* user who triggered action */
    "userId": 00000000, /* user who triggered action */
    "isSubscribed": true,
    "isModerator": false,
    "isVip": false,
    "broadcastUser": "nate1280",
    "broadcastUserName": "nate1280",
    "broadcastUserId": 00000000,
    "broadcasterIsAffiliate": true,
    "broadcasterIsPartner": false,
    "randomUser0": "<user's display name>",
    "randomUserName0": "<username>",
    "randomUserId0": 00000000,
    "randomUser1": "<user's display name>",
    "randomUserName1": "<username>",
    "randomUserId1": 00000000,
    "randomUser2": "<user's display name>",
    "randomUserName2": "<username>",
    "randomUserId2": 00000000
  },
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": true,
    "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
  }
}
```
---
navigation.title: Twitch
---

# Twitch Events
Reference of all Twitch events emitted by the WebSocket Server.


## Follow
```json [Follow]
{
  "userId": 0000000,
  "userName": "<username>",
  "displayName": "<display name>",
  "isTest": true|false
}
```

## Cheer
```json [Cheer]
{
  "message": {
    "msgId": "21605e47-16d2-4496-8001-509438e1b41c",
    "userId": 00000000
    "username": "<username>",
    "role": 1, /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
    "subscriber": true,
    "displayName": "<display name of cheerer>",
    "channel": "<channel>",
    "message": "<message that contained the cheer>",
    "isHighlighted": false,
    "isMe": false,
    "isCustomReward": false,
    "isAnonymous": false,
    "isReply": false,
    "bits": 42,
    "hasBits": true,
    "emotes": [],
    "cheerEmotes": [
      {
        "bits": 42,
        "color": "#979797",
        "type": "CheerEmote",
        "name": "Cheer",
        "startIndex": 0,
        "endIndex": 6,
        "imageUrl": "<url to cheer emote>"
      }
    ]
  }
}
```

## Raid
```json [Raid]
{
  "viewerCount": 42,
  "profileImage": "test.png",
  "userId": 0000000,
  "userName": "<username>",
  "displayName": "<display name>",
  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
}
```

## Stream Update
```json [StreamUpdate]
{
  "channelId": 0000000000,
  "channel": "<user name of broadcaster>",
  "status": "Doing the things!", /* New title of the stream */
  "oldStatus": "This is a different title!", /* Old title of the stream */
  "oldGame": {
    "id": 516097,
    "name": "Deadside"
  },
  "game": {
    "id": 7658,
    "name": "Mario Party 8"
  }
}
```

## Whisper
```json [Whisper]
{
  "message": {
    "msgId": "60",
    "userId": 00000000,
    "username": "<username>",
    "displayName": "<user's display name>",
    "message": "Test",
    "emotes": []
  }
}
```

## First Words
```json [FirstWord]
{
  "message": "test",
  "action": false,
  "user": {
    "id": 0000000000,
    "login": "<username>",
    "display_name": "<displayname>",
    "subscribed": true,
    "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
  }
}
```

## Chat Message
```json [ChatMessage]
{
  "message": {
    "msgId": "a0d32df1-d3ca-4fd7-87fb-6c4e958550f0",
    "userId": 00000000,
    "username": "<username>",
    "role": 4,
    "subscriber": true,
    "displayName": "<display name>",
    "channel": "<broadcaster's channel name>",
    "message": "", /* The message the user sent */
    "isHighlighted": false,
    "isMe": false,
    "isCustomReward": false,
    "isAnonymous": false,
    "isReply": false,
    "bits": 0,
    "hasBits": false,
    "emotes": [
      {
        "id": "300400304",
        "type": "Twitch",
        "name": "nate121Raid",
        "startIndex": 5,
        "endIndex": 15,
        "imageUrl": "https://static-cdn.jtvnw.net/emoticons/v2/300400304/default/dark/2.0"
      }
    ],
    "cheerEmotes": []
  }
}
```

## Ad Run
```json
{
  "length": 90,
  "scheduled": false
}
```

## Subscriptions

### Sub
```json
{
  "subTier": 0, /* 0 - Prime, 1 - Tier 1, 2 - Tier 2, 3 - Tier 3 */
  "color": "#008D99",
  "emotes": [],
  "message": "",
  "userId": 00000000,
  "userName": "<username>",
  "displayName": "<display name>",
  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
}
```

### Resub
```json
{
  "cumulativeMonths": 25,
  "shareStreak": true,
  "streakMonths": 1,
  "subTier": 0, /* 0 - Prime, 1 - Tier 1, 2 - Tier 2, 3 - Tier 3 */
  "color": "#FF4500",
  "emotes": [],
  "message": "",
  "userId": 162909743,
  "userName": "admiralai",
  "displayName": "AdmiralAI",
  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
}
```

### Gift Sub
```json
{
  "isAnonymous": false,
  "totalSubsGifted": 1,
  "cumulativeMonths": 4,
  "monthsGifted": 1,
  "fromSubBomb": false,
  "subBombCount": 1,
  "recipientUserId": 00000000,
  "recipientUsername": "<username of recipient>",
  "recipientDisplayName": "<display name of recipient>",
  "subTier": 0, /* 0 - Prime, 1 - Tier 1, 2 - Tier 2, 3 - Tier 3 */
  "userId": 0000000000,
  "userName": "<username of gifter>",
  "displayName": "<displayname of gifter>",
  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
}
```

### Gift Bomb
```json
{
  "isAnonymous": false,
  "gifts": 10,
  "totalGifts": 0,
  "subTier": 0, /* 0 - Prime, 1 - Tier 1, 2 - Tier 2, 3 - Tier 3 */
  "userId": 0000000000,
  "userName": "<username of gifter>",
  "displayName": "<displayname of gifter>",
  "role": 1 /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
}
```

## Hype Train
### Hype Train Start
```json
{
  "level": 1,
  "levelGoal": 3500,
  "levelTotal": 3900,
  "totalGoal": 11500,
  "total": 11100,
  "percent": 1.1142857142857143
}
```

### Hype Train Update
```json
{
  "userId": 00000000,
  "level": 1,
  "contributors": 1,
  "levelGoal": 3500,
  "levelTotal": 3900,
  "totalGoal": 11500,
  "total": 11100,
  "percent": 1.1142857142857143
}
```

### Hype Train Level Up
```json
{
  "prevLevel": 0,
  "level": 1,
  "contributors": 0,
  "levelGoal": 3500,
  "levelTotal": 3900,
  "totalGoal": 11500,
  "total": 11100,
  "percent": 1.1142857142857143
}
```

### Hype Train End
```json
 {
   "conductor": {
     "id": 0 /* the twitch user id of the conductor */
   },
   "level": 1,
   "contributorCount": 1,
   "contributors": [
     {
       "id": 00000000
     }
   ],
   "levelGoal": 3500,
   "levelTotal": 3900,
   "totalGoal": 11500,
   "total": 11100,
   "percent": 1.1142857142857143
 }
```

## Channel Point Rewards

### Reward Redemption
```json
 {
   "id": "9d0911db-7884-4e0f-8cf4-c95c5765c2e5",
   "dateTime": "2022-01-31T03:10:23.3611616Z",
   "userId": 0000000000,
   "userName": "<user name of redeemer>",
   "displayName": "<display name of redeemer>",
   "channelId": 0000000, /* broadcaster channel id */
   "cost": 42,
   "rewardId": "41f257e9-9688-4944-9bf6-28cda1c3fa1f",
   "title": "Test Reward",
   "prompt": "",
   "inputRequired": false,
   "backgroundColor": "#63D0A9",
   "enabled": true,
   "paused": false,
   "subOnly": false
 }
```

### Reward Created
```json
{
  "id": "41f257e9-9688-4944-9bf6-28cda1c3fa1f",
  "name": "Test Reward",
  "prompt": "",
  "group": "",
  "cost": 42,
  "userInput": false,
  "persistCounter": false,
  "counter": 1,
  "persistUserCounter": false,
  "backgroundColor": "#63D0A9",
  "userCounters": {}
}
```

### Reward Updated
```json
{
  "dateTime": "2022-01-31T03:10:10.9796761Z",
  "channelId": 00000000,
  "cost": 42,
  "rewardId": "41f257e9-9688-4944-9bf6-28cda1c3fa1f",
  "title": "Test Reward",
  "prompt": "",
  "inputRequired": false,
  "backgroundColor": "#63D0A9",
  "enabled": true,
  "paused": true,
  "subOnly": false
}
```

### Reward Deleted
```json
{
  "dateTime": "2022-01-31T03:18:07.6679489Z",
  "channelId": 00000000,
  "cost": 42,
  "rewardId": "d52a0894-586e-4943-9027-385e8ea04f79",
  "title": "Test Reward",
  "prompt": "",
  "inputRequired": false
}
```

## Community Goals
### Community Goal Contribution
```json
{
  "dateTime": "",
  "channelId": 0,
  "id": "",
  "title": "",
  "description": "",
  "inStock": true,
  "amount": 0, /* total amount required to complete goal */
  "contributed": 0, /* how much has been contributed so far */
  "duration": 0,
  "startedAt": "",
  "endedAt": "",
  "daysLeft": 0,
  "userId": 00000000,
  "userName": "<username>",
  "displayName": "<user's display name>",
  "userContributed": 0, /* hopw much the user contributed */
  "userStreamContributed": 0, /* hopw much the user contributed this stream */
  "userTotalContributed": 0, /* hopw much the user contributed for the entire goal */
}
```

### Community Goal Ended
```json
{
  "dateTime": "",
  "channelId": 0,
  "id": "",
  "title": "",
  "description": "",
  "inStock": true,
  "amount": 0, /* total amount required to complete goal */
  "contributed": 0, /* how much has been contributed so far */
  "duration": 0,
}
```

## Polls
### Poll Created
```json
{
  "dateTime": "2022-01-30T22:20:28.5021247-05:00",
  "channelId": 00000000,
  "type": 1,
  "id": "6e3b2f5b-39f1-4b09-b9aa-9937a289571b",
  "title": "Test Poll",
  "startedAt": "2022-01-31T03:20:28.5218414Z",
  "duration": 60,
  "settings": {
    "multi_choice": {
      "is_enabled": true
    },
    "subscriber_only": {
      "is_enabled": false
    },
    "subscriber_multiplier": {
      "is_enabled": false
    },
    "bits_votes": {
      "cost": 0,
      "is_enabled": false
    },
    "channel_points_votes": {
      "cost": 0,
      "is_enabled": false
    }
  },
  "choices": [
    {
      "choice_id": "be5bde15-d779-43f4-8065-a5467810aeac",
      "title": "Option 1",
      "votes": {
        "total": 0,
        "base": 0,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 0
    },
    {
      "choice_id": "f995c9fb-47ef-41e3-aeab-33ed5b2083e2",
      "title": "Option 2",
      "votes": {
        "total": 0,
        "base": 0,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 0
    }
  ],
  "votes": {
    "total": 0,
    "base": 0,
    "bits": 0,
    "channel_points": 0
  },
  "tokens": {
    "bits": 0,
    "channel_points": 0
  },
  "totalVotes": 0,
  "remainingDurationMilliseconds": 59984
}
```

### Poll Updated
```json
{
  "dateTime": "2022-01-30T22:20:35.2286411-05:00",
  "channelId": 00000000,
  "type": 2,
  "id": "6e3b2f5b-39f1-4b09-b9aa-9937a289571b",
  "title": "Test Poll",
  "startedAt": "2022-01-31T03:20:28.5218414Z",
  "duration": 60,
  "settings": {
    "multi_choice": {
      "is_enabled": true
    },
    "subscriber_only": {
      "is_enabled": false
    },
    "subscriber_multiplier": {
      "is_enabled": false
    },
    "bits_votes": {
      "cost": 0,
      "is_enabled": false
    },
    "channel_points_votes": {
      "cost": 0,
      "is_enabled": false
    }
  },
  "choices": [
    {
      "choice_id": "be5bde15-d779-43f4-8065-a5467810aeac",
      "title": "Option 1",
      "votes": {
        "total": 1,
        "base": 1,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 1
    },
    {
      "choice_id": "f995c9fb-47ef-41e3-aeab-33ed5b2083e2",
      "title": "Option 2",
      "votes": {
        "total": 0,
        "base": 0,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 0
    }
  ],
  "votes": {
    "total": 1,
    "base": 1,
    "bits": 0,
    "channel_points": 0
  },
  "tokens": {
    "bits": 0,
    "channel_points": 0
  },
  "totalVotes": 1,
  "remainingDurationMilliseconds": 53240
}
```

### Poll Completed
```json
{
  "endedAt": "2022-01-31T03:21:28.5218414Z",
  "winningChoice": {
    "choice_id": "be5bde15-d779-43f4-8065-a5467810aeac",
    "title": "Option 1",
    "votes": {
      "total": 1,
      "base": 1,
      "bits": 0,
      "channel_points": 0
    },
    "tokens": {
      "bits": 0,
      "channel_points": 0
    },
    "total_voters": 1
  },
  "dateTime": "2022-01-30T22:21:28.8137307-05:00",
  "channelId": 00000000,
  "type": 4,
  "id": "6e3b2f5b-39f1-4b09-b9aa-9937a289571b",
  "title": "Test Poll",
  "startedAt": "2022-01-31T03:20:28.5218414Z",
  "duration": 60,
  "settings": {
    "multi_choice": {
      "is_enabled": true
    },
    "subscriber_only": {
      "is_enabled": false
    },
    "subscriber_multiplier": {
      "is_enabled": false
    },
    "bits_votes": {
      "cost": 0,
      "is_enabled": false
    },
    "channel_points_votes": {
      "cost": 0,
      "is_enabled": false
    }
  },
  "choices": [
    {
      "choice_id": "be5bde15-d779-43f4-8065-a5467810aeac",
      "title": "Option 1",
      "votes": {
        "total": 1,
        "base": 1,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 1
    },
    {
      "choice_id": "f995c9fb-47ef-41e3-aeab-33ed5b2083e2",
      "title": "Option 2",
      "votes": {
        "total": 0,
        "base": 0,
        "bits": 0,
        "channel_points": 0
      },
      "tokens": {
        "bits": 0,
        "channel_points": 0
      },
      "total_voters": 0
    }
  ],
  "votes": {
    "total": 1,
    "base": 1,
    "bits": 0,
    "channel_points": 0
  },
  "tokens": {
    "bits": 0,
    "channel_points": 0
  },
  "totalVotes": 1,
  "remainingDurationMilliseconds": 0
}
```

## Predictions
### Prediction Created
```json
{
  "outcomes": [
    {
      "id": "8402eed1-19c3-4a1a-b728-1148273d31e4",
      "color": "BLUE",
      "title": "Outcome 1",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    },
    {
      "id": "b26ab426-03c0-46a7-a109-313b8b1cda7a",
      "color": "PINK",
      "title": "Outcome 2",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    }
  ],
  "dateTime": "2022-01-30T22:22:08.8207639-05:00",
  "channelId": 000000,
  "type": 1,
  "status": 1,
  "id": "f6205b82-2fd9-446b-abc0-70d02ab44ba7",
  "title": "Test Prediction",
  "createdAt": "2022-01-31T03:22:08.8386896Z",
  "createdBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<username of creator>"
  },
  "predictionWindow": 60
}
```

### Prediction Updated
```json
{
  "outcomes": [
    {
      "id": "8402eed1-19c3-4a1a-b728-1148273d31e4",
      "color": "BLUE",
      "title": "Outcome 1",
      "total_points": 10,
      "total_users": 1,
      "top_predictors": [
        {
          "event_id": "f6205b82-2fd9-446b-abc0-70d02ab44ba7",
          "outcome_id": "8402eed1-19c3-4a1a-b728-1148273d31e4",
          "channel_id": 00000000,
          "points": 10,
          "predicted_at": "2022-01-31T03:22:52.1304709Z",
          "updated_at": "2022-01-31T03:22:52.1304709Z",
          "user_id": 00000000,
          "user_display_name": "<user's display name>"
        }
      ]
    },
    {
      "id": "b26ab426-03c0-46a7-a109-313b8b1cda7a",
      "color": "PINK",
      "title": "Outcome 2",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    }
  ],
  "dateTime": "2022-01-30T22:22:53.2067849-05:00",
  "channelId": 00000000,
  "type": 2,
  "status": 1,
  "id": "f6205b82-2fd9-446b-abc0-70d02ab44ba7",
  "title": "Test Prediction",
  "createdAt": "2022-01-31T03:22:08.8386896Z",
  "createdBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "predictionWindow": 60
}
```

### Prediction Completed
```json
{
  "outcomes": [
    {
      "id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
      "color": "BLUE",
      "title": "Outcome 1",
      "total_points": 10,
      "total_users": 1,
      "top_predictors": [
        {
          "event_id": "33b85949-83db-4683-bf5f-1ab3a00188cb",
          "outcome_id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
          "channel_id": 00000000,
          "points": 10,
          "predicted_at": "2022-01-31T03:23:15.2948659Z",
          "updated_at": "2022-01-31T03:23:15.2948659Z",
          "user_id": 00000000,
          "user_display_name": "<user's display name>"
        }
      ]
    },
    {
      "id": "d9bf57ec-3817-458b-8728-f7d81e8abc51",
      "color": "PINK",
      "title": "Outcome 2",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    }
  ],
  "winningOutcomeId": "8c0c876a-4c43-42eb-aee6-6dd787434610",
  "winningOutcome": {
    "id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
    "color": "BLUE",
    "title": "Outcome 1",
    "total_points": 10,
    "total_users": 1,
    "top_predictors": [
      {
        "event_id": "33b85949-83db-4683-bf5f-1ab3a00188cb",
        "outcome_id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
        "channel_id": 00000000,
        "points": 10,
        "predicted_at": "2022-01-31T03:23:15.2948659Z",
        "updated_at": "2022-01-31T03:23:15.2948659Z",
        "user_id": 00000000,
        "user_display_name": "<user's display name>"
      }
    ]
  },
  "dateTime": "2022-01-30T22:23:25.8367758-05:00",
  "channelId": 00000000,
  "type": 2,
  "status": 4,
  "id": "33b85949-83db-4683-bf5f-1ab3a00188cb",
  "title": "Test Prediction",
  "createdAt": "2022-01-31T03:23:07.8904015Z",
  "endedAt": "2022-01-31T03:23:25.1085385Z",
  "lockedAt": "2022-01-31T03:23:22.8303546Z",
  "createdBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "endedBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "lockedBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "predictionWindow": 60
}
```

### Prediction Canceled
```json
{
  "outcomes": [
    {
      "id": "8402eed1-19c3-4a1a-b728-1148273d31e4",
      "color": "BLUE",
      "title": "Outcome 1",
      "total_points": 10,
      "total_users": 1,
      "top_predictors": [
        {
          "event_id": "f6205b82-2fd9-446b-abc0-70d02ab44ba7",
          "outcome_id": "8402eed1-19c3-4a1a-b728-1148273d31e4",
          "channel_id": 00000000,
          "points": 10,
          "predicted_at": "2022-01-31T03:22:52.1304709Z",
          "updated_at": "2022-01-31T03:22:52.1304709Z",
          "user_id": 00000000,
          "user_display_name": "<user's display name>"
        }
      ]
    },
    {
      "id": "b26ab426-03c0-46a7-a109-313b8b1cda7a",
      "color": "PINK",
      "title": "Outcome 2",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    }
  ],
  "dateTime": "2022-01-30T22:23:04.5190145-05:00",
  "channelId": 0000000,
  "type": 2,
  "status": 6,
  "id": "f6205b82-2fd9-446b-abc0-70d02ab44ba7",
  "title": "Test Prediction",
  "createdAt": "2022-01-31T03:22:08.8386896Z",
  "endedAt": "2022-01-31T03:23:03.618273Z",
  "createdBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "endedBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "predictionWindow": 60
}
```

### Prediction Locked
```json
{
  "outcomes": [
    {
      "id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
      "color": "BLUE",
      "title": "Outcome 1",
      "total_points": 10,
      "total_users": 1,
      "top_predictors": [
        {
          "event_id": "33b85949-83db-4683-bf5f-1ab3a00188cb",
          "outcome_id": "8c0c876a-4c43-42eb-aee6-6dd787434610",
          "channel_id": 00000000,
          "points": 10,
          "predicted_at": "2022-01-31T03:23:15.2948659Z",
          "updated_at": "2022-01-31T03:23:15.2948659Z",
          "user_id": 00000000,
          "user_display_name": "<user's display name>"
        }
      ]
    },
    {
      "id": "d9bf57ec-3817-458b-8728-f7d81e8abc51",
      "color": "PINK",
      "title": "Outcome 2",
      "total_points": 0,
      "total_users": 0,
      "top_predictors": []
    }
  ],
  "winningOutcomeId": "00000000-0000-0000-0000-000000000000",
  "dateTime": "2022-01-30T22:23:22.7880889-05:00",
  "channelId": 00000000,
  "type": 2,
  "status": 2,
  "id": "33b85949-83db-4683-bf5f-1ab3a00188cb",
  "title": "Test Prediction",
  "createdAt": "2022-01-31T03:23:07.8904015Z",
  "lockedAt": "2022-01-31T03:23:22.8303546Z",
  "createdBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "lockedBy": {
    "type": "USER",
    "user_id": 00000000,
    "user_display_name": "<user's display name>"
  },
  "predictionWindow": 60
}
```
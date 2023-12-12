---
navigation.title: Twitch
---

# Twitch Events
Reference of all Twitch events emitted by the WebSocket Server.


## Follow
```json [Follow]
{
  "user_id": "00000000",
  "user_login": "<username>",
  "user_name": "<display name>",
  "followed_at": "2023-12-11T18:36:21.616161Z" /*ISO 8601 formatted "YYYY-MM-DDTHH:MM:SS.SSSSSSZ" */
}
```

## Cheer
```json [Cheer]
{
  "message": {
    "internal": false,
    "msgId": "21605e47-16d2-4496-8001-509438e1b41c",
    "userId": "00000000",
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
    "firstMessage": false,
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
    ],
    "badges": [
      {
        "name": "<type of badge>", /* e.g. : subscriber, bits-leader etc... */
        "version": "0",
        "imageUrl": "<url to cheerer badge>"
      }
    ],
    "monthsSubscribed": 6,
    "isTest": true
   }
}

```

## Raid
```json [Raid]
{
  "from_broadcaster_user_id": "00000000", /* the streamer raiding */
  "from_broadcaster_user_login": "<username>",
  "from_broadcaster_user_name": "<display name>",
  "to_broadcaster_user_id": "00000000", /* the streamer being raided */
  "to_broadcaster_user_login": "<username>",
  "to_broadcaster_user_name": "<display name>",
  "viewers": 10
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

### BotWhisper
```json [BotWhisper]
{
  "command": "!bots",
  "counter": 1,
  "userCounter": 1,
  "message": "",
  "user": {
    "id": 00000000,
    "login": "<username>",
    "display_name": "<user's display name>",
    "subscribed": true,
    "role": 4
  }
}
```

## First Words
```json [FirstWord]
{
   "message":{
      "internal":false,
      "msgId":"fa827baf-27b3-470d-be87-3ecda0ecf5b3",
      "userId":"00000000",
      "username":"<username>",
      "role":1,
      "subscriber":false,
      "displayName":"<display name>",
      "color":"#9ACD32",
      "channel":"<broadcaster username>",
      "message":"First Words Test Message",
      "isHighlighted":false,
      "isMe":false,
      "isCustomReward":false,
      "isAnonymous":false,
      "isReply":false,
      "bits":0,
      "firstMessage":false,
      "hasBits":false,
      "emotes":[],
      "cheerEmotes":[],
      "badges":[],
      "monthsSubscribed":0,
      "isTest":false
   }
}
```

## Chat Message
```json [ChatMessage]
{
   "message":{
      "internal":false,
      "msgId":"e7690013-be86-43e6-8056-00e7e95c9351",
      "userId":"00000000",
      "username":"<username>",
      "role":1,
      "subscriber":false,
      "displayName":"<display name>",
      "color":"#9ACD32",
      "channel":"<broadcaster username>",
      "message":"random message test",
      "isHighlighted":false,
      "isMe":false,
      "isCustomReward":false,
      "isAnonymous":false,
      "isReply":false,
      "bits":0,
      "firstMessage":false,
      "hasBits":false,
      "emotes":[],
      "cheerEmotes":[],
      "badges":[],
      "monthsSubscribed":0,
      "isTest":false
   }
}
```


```json [AdRun]
{
  "length": 90,
  "scheduled": false
}
```
```json [AdMidRoll]
{
  "jitterTime": 5000,
  "warmupTime": 5000,
  "commercialId": "9b2af8e9-7266-4ea8-bf94-fd615ad40aae"
}
```

## Subscriptions

```json [Sub]
{
  "subTier":1,
      "emotes": [],
      "badges": [],
      "message": "Test Subscription",
      "userId": "00000000",
      "userName": "<subscriber's username>",
      "displayName": "<subscriber's display name>",
      "role": 0, /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
      "isTest": true
}
```


```json [Resub]
{
  "cumulativeMonths": 0,
  "shareStreak": false,
  "streakMonths": 0,
  "subTier": 3,
  "emotes": [],
  "badges": [],
  "message": "test message",
  "userId": "00000000",
  "userName": "<subscriber's username>",
  "displayName": "<subscriber's display name>",
  "role": 0, /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
  "isTest": true
}
```

```json [GiftSub]
{
  "isAnonymous": false,
  "totalSubsGifted": 0,
  "cumulativeMonths": 0,
  "monthsGifted": 12,
  "fromSubBomb": false,
  "subBombCount": 0,
  "recipientUserId": "00000000",
  "recipientUsername": "<username>",
  "recipientDisplayName": "<display name>",
  "subTier": 2,
  "emotes": [],
  "badges": [],
  "userId": "00000000",
  "userName": "<gifter's username>",
  "displayName": "<gifter's display name>",
  "role": 0, /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
  "isTest": true
}
```

```json [GiftBomb]
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

```json [HypeTrainStart]
{
  "level": 1,
  "progress": 10,
  "last_contribution": {
    "user_id": "00000000",
    "user_login": "<username>",
    "user_name": "<displayname>",
    "total": 0
  },
  "expires_at": "2023-12-11T21:38:20.0529012Z", /*ISO 8601 formatted "YYYY-MM-DDTHH:MM:SS.SSSSSSZ" */
  "isTest": true,
  "id": "1c5a382d-20c0-4071-96be-925e0e0b63da",
  "total": 0,
  "goal": 1000,
  "top_contributions": [
    {
      "user_id": "00000000",
      "user_login": "<username>",
      "user_name": "<displayname>",
      "type": "bits",
      "total": 100
    }
  ],
  "started_at":"2023-12-11T21:36:20.0529012Z" /*ISO 8601 formatted "YYYY-MM-DDTHH:MM:SS.SSSSSSZ" */
}
```


```json [HypeTrainUpdate]
{
  "level": 1,
  "progress": 10,
  "last_contribution": {
    "user_id": "00000000",
    "user_login": "<username>",
    "user_name": "<displayname>",
    "total": 0
  },
  "expires_at": "2023-12-11T21:40:32.2640462Z", /*ISO 8601 formatted "YYYY-MM-DDTHH:MM:SS.SSSSSSZ" */
  "isTest": true,
  "id": "7067ae5d-4d79-4a56-bfce-8478a9654a11",
  "total": 0,
  "goal": 1000,
  "top_contributions": [
    {
      "user_id": "00000000",
      "user_login": "<username>",
      "user_name": "<displayname>",
      "type": "bits",
      "total": 100
    }
  ],
  "started_at": "2023-12-11T21:38:32.2640462Z" /*ISO 8601 formatted "YYYY-MM-DDTHH:MM:SS.SSSSSSZ" */
}
```


```json [HypeTrainLevelUp]
{
  "level": 1,
  "progress": 10,
  "last_contribution": {
    "user_id": "00000000",
    "user_login": "<username>",
    "user_name": "<displayname>",
    "total": 0
  },
  "expires_at": "2023-12-11T21:49:17.4764711Z", /*ISO 8601 formatted "YYYY-MM-DDTHH:MM:SS.SSSSSSZ" */
  "isTest": true,
  "id": "4eee4a40-03d0-4862-bb45-7300f6c01fc3",
  "total": 0,
  "goal": 1000,
  "top_contributions": [
    {
      "user_id": "00000000",
      "user_login": "<username>",
      "user_name": "<displayname>",
      "type": "bits",
      "total": 100
    }
  ],
  "started_at": "2023-12-11T21:47:17.4764711Z" /*ISO 8601 formatted "YYYY-MM-DDTHH:MM:SS.SSSSSSZ" */
}
```

```json [HypeTrainEnd]
{
  "level": 1,
  "ended_at": "2023-12-11T21:49:51.483657Z", /*ISO 8601 formatted "YYYY-MM-DDTHH:MM:SS.SSSSSSZ" */
  "cooldown_ends_at": "2023-12-11T21:59:51.483657Z", /*ISO 8601 formatted "YYYY-MM-DDTHH:MM:SS.SSSSSSZ" */
  "isTest": true,
  "id": "8e2a4863-62a0-4716-a9fa-9a21c79c101f",
  "total": 1000,
  "goal": 0,
  "top_contributions": [
    {
      "user_id": "646848961",
      "user_login": "<username>",
      "user_name": "<displayname>",
      "type": "bits",
      "total": 100
    }
  ],
  "started_at": "2023-12-11T21:44:51.483657Z" /*ISO 8601 formatted "YYYY-MM-DDTHH:MM:SS.SSSSSSZ" */
}
```

## Channel Point Rewards

```json [RewardRedemption]
{
   "id":"cbe54e38-0716-43cc-b5cb-c6639968a479",
   "user_id":"00000000",
   "user_login":"<user name of redeemer>",
   "user_name":"<display name of redeemer>",
   "user_input":"",
   "status":"unfulfilled",
   "reward":{
      "id":"c125c87b-2da0-46f4-8575-8433580cccbf",
      "title":"updated title test",
      "cost":11,
      "prompt":"updated Prompt test"
   },
   "redeemed_at":"2023-12-12T07:50:13.8014246Z"
}
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

```json [RewardCreated]
{
   "id":"c125c87b-2da0-46f4-8575-8433580cccbf",
   "name":"Test Title",
   "prompt":"Test Prompt",
   "group":"Test Group",
   "cost":1,
   "userInput":false,
   "persistCounter":false,
   "persistUserCounter":false,
   "backgroundColor":"#C26E73"
}
```

```json [RewardUpdated]
{
   "id":"c125c87b-2da0-46f4-8575-8433580cccbf",
   "is_enabled":true,
   "is_paused":false,
   "is_in_stock":true,
   "title":"updated title test",
   "cost":11,
   "prompt":"updated Prompt test",
   "is_user_input_required":false,
   "should_redemptions_skip_request_queue":false,
   "max_per_stream":{
      "is_enabled":false,
      "value":0
   },
   "max_per_user_per_stream":{
      "is_enabled":false,
      "value":0
   },
   "global_cooldown":{
      "is_enabled":false,
      "seconds":0
   },
   "background_color":"#C26E73",
   "default_image":{
      "url_1x":"https://static-cdn.jtvnw.net/custom-reward-images/default-1.png",
      "url_2x":"https://static-cdn.jtvnw.net/custom-reward-images/default-2.png",
      "url_4x":"https://static-cdn.jtvnw.net/custom-reward-images/default-4.png"
   }
}
```

```json [RewardDeleted]
{
   "id":"c125c87b-2da0-46f4-8575-8433580cccbf",
   "is_enabled":true,
   "is_paused":false,
   "is_in_stock":true,
   "title":"updated title test",
   "cost":11,
   "prompt":"updated Prompt test",
   "is_user_input_required":false,
   "should_redemptions_skip_request_queue":false,
   "max_per_stream":{
      "is_enabled":false,
      "value":0
   },
   "max_per_user_per_stream":{
      "is_enabled":false,
      "value":0
   },
   "global_cooldown":{
      "is_enabled":false,
      "seconds":0
   },
   "background_color":"#C26E73",
   "default_image":{
      "url_1x":"https://static-cdn.jtvnw.net/custom-reward-images/default-1.png",
      "url_2x":"https://static-cdn.jtvnw.net/custom-reward-images/default-2.png",
      "url_4x":"https://static-cdn.jtvnw.net/custom-reward-images/default-4.png"
   }
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
```json [PollCreated]
{
   "ends_at":"2023-12-12T07:22:33.9991669Z",
   "id":"ce4a2a0d-409f-49d1-b569-5e2087dd95db",
   "title":"Test Question",
   "choices":[ /* up to 5 choices */
      {
         "id":"31bdb9f2-1449-4d51-969e-b04a34585a32",
         "title":"Test Response 1",
         "channel_points_votes":0,
         "votes":0
      },
      {
         "id":"73a421a4-0f6e-4892-96d3-a00bf44d55f1",
         "title":"Test Response 2",
         "channel_points_votes":0,
         "votes":0
      }
   ],
   "channel_points_voting":{
      "is_enabled":true,
      "amount_per_vote":200
   },
   "started_at":"2023-12-12T07:21:33.9991669Z"
}
```

```json [PollUpdated]
{
   "ends_at":"2023-12-12T07:25:18.7915934Z",
   "id":"301066b9-f1ca-4755-a03e-0ac8b1664855",
   "title":"test question",
   "choices":[
      {
         "id":"40fb5b0a-55b3-4bdd-8447-7d8561d89cb2",
         "title":"test response 1",
         "channel_points_votes":1,
         "votes":2
      },
      {
         "id":"40ee04f5-224c-44ce-8697-2c6758ad509f",
         "title":"test response 2",
         "channel_points_votes":0,
         "votes":0
      }
   ],
   "channel_points_voting":{
      "is_enabled":true,
      "amount_per_vote":200
   },
   "started_at":"2023-12-12T07:24:18.7915934Z"
}
```

```json [PollCompleted]
{
   "status":"completed",
   "ended_at":"2023-12-12T07:25:18.7915934Z",
   "winningChoice":{
      "id":"40fb5b0a-55b3-4bdd-8447-7d8561d89cb2",
      "title":"test response 1",
      "channel_points_votes":1,
      "votes":2
   },
   "id":"301066b9-f1ca-4755-a03e-0ac8b1664855",
   "title":"test question",
   "choices":[
      {
         "id":"40fb5b0a-55b3-4bdd-8447-7d8561d89cb2",
         "title":"test response 1",
         "channel_points_votes":1,
         "votes":2
      },
      {
         "id":"40ee04f5-224c-44ce-8697-2c6758ad509f",
         "title":"test response 2",
         "channel_points_votes":0,
         "votes":0
      }
   ],
   "channel_points_voting":{
      "is_enabled":true,
      "amount_per_vote":200
   },
   "started_at":"2023-12-12T07:24:18.7915934Z"
}
```

## Predictions

```json [PredictionCreated]
{
   "locks_at":"2023-12-12T06:26:40.6062778Z",
   "id":"52e6b1e1-4e4d-4eef-8b4a-249be8fc1e3c",
   "title":"Prediction -> Question 2 Choices Template",
   "outcomes":[
      {
         "id":"cc967dbc-9dcc-4ce4-bae5-8cb2d754915c",
         "title":"choice 1",
         "color":"blue",
         "users":0,
         "channel_points":0
      },
      {
         "id":"3d5faef0-cccb-4ce2-809c-c76ddbd3df43",
         "title":"choice 2",
         "color":"pink", /* if more than 2 choices all colors are "blue" */
         "users":0,
         "channel_points":0
      }
   ],
   "started_at":"2023-12-12T06:25:40.6062778Z"
}
```

```json [PredictionUpdated]
{
   "locks_at":"2023-12-12T06:50:42.2681038Z",
   "id":"5a93f9d8-5c1a-40d1-bbeb-d75a98f4396b",
   "title":"Prediction -> Question 2 Choices Template",
   "outcomes":[
      {
         "id":"2e4fbe22-72ad-4dda-9335-b0caee2ca649",
         "title":"choice 1",
         "color":"blue",
         "users":1,
         "channel_points":10,
         "top_predictors":[ /* up to 3 */
            {
               "user_id":"00000000",
               "user_login":"<username>",
               "user_name":"<displayname>",
               "channel_points_used":10
            }
         ]
      },
      {
         "id":"f022cb9a-440b-4532-9e68-1cafce75cd5b",
         "title":"choice 2",
         "color":"pink",
         "users":0,
         "channel_points":0,
         "top_predictors":[] /* up to 3 */
      }
   ],
   "started_at":"2023-12-12T06:49:42.2681038Z"
}
```

```json [PredictionCompleted]
{
   "winning_outcome_id":"2e4fbe22-72ad-4dda-9335-b0caee2ca649",
   "status":"resolved",
   "ended_at":"2023-12-12T06:54:57.6794341Z",
   "winning_outcome":{
      "id":"2e4fbe22-72ad-4dda-9335-b0caee2ca649",
      "title":"choice 1",
      "color":"blue",
      "users":1,
      "channel_points":10,
      "top_predictors":[ /* up to 3 */
         {
            "user_id":"00000000",
            "user_login":"<username>",
            "user_name":"<displayname>",
            "channel_points_won":10,
            "channel_points_used":10
         }
      ]
   },
   "id":"5a93f9d8-5c1a-40d1-bbeb-d75a98f4396b",
   "title":"Prediction -> Question 2 Choices Template",
   "outcomes":[
      {
         "id":"2e4fbe22-72ad-4dda-9335-b0caee2ca649",
         "title":"choice 1",
         "color":"blue",
         "users":1,
         "channel_points":10,
         "top_predictors":[ /* up to 3 */
            {
               "user_id":"00000000",
               "user_login":"<username>",
               "user_name":"<displayname>",
               "channel_points_won":10,
               "channel_points_used":10
            }
         ]
      },
      {
         "id":"f022cb9a-440b-4532-9e68-1cafce75cd5b",
         "title":"choice 2",
         "color":"pink",
         "users":0,
         "channel_points":0,
         "top_predictors":[]
      }
   ],
   "started_at":"2023-12-12T06:49:42.2681038Z"
}
```

```json [PredictionCanceled]
{
   "winning_outcome_id":"",
   "status":"canceled",
   "ended_at":"2023-12-12T07:05:25.3009388Z",
   "id":"f3e18d41-98e9-41c2-bce1-86d3e74bdd2a",
   "title":"Prediction -> Question 2 Choices Template",
   "outcomes":[
      {
         "id":"b8a62255-8821-40e3-b598-a38466d5317d",
         "title":"choice 1",
         "color":"blue",
         "users":1,
         "channel_points":10,
         "top_predictors":[ /* up to 3 */
            {
               "user_id":"00000000",
               "user_login":"<username>",
               "user_name":"<displayname>",
               "channel_points_won":0,
               "channel_points_used":10
            }
         ]
      },
      {
         "id":"6c7c4143-7a99-46bc-8df3-4106b61ec87f",
         "title":"choice 2",
         "color":"pink",
         "users":0,
         "channel_points":0,
         "top_predictors":[]
      }
   ],
   "started_at":"2023-12-12T07:05:08.2264206Z"
}
```

```json [PredictionLocked]
{
   "locked_at":"2023-12-12T06:50:41.4081242Z",
   "id":"5a93f9d8-5c1a-40d1-bbeb-d75a98f4396b",
   "title":"Prediction -> Question 2 Choices Template",
   "outcomes":[
      {
         "id":"2e4fbe22-72ad-4dda-9335-b0caee2ca649",
         "title":"choice 1",
         "color":"blue",
         "users":1,
         "channel_points":10,
         "top_predictors":[ /* up to 3 */
            {
               "user_id":"00000000",
               "user_login":"<username>",
               "user_name":"<displayname>",
               "channel_points_used":10
            }
         ]
      },
      {
         "id":"f022cb9a-440b-4532-9e68-1cafce75cd5b",
         "title":"choice 2",
         "color":"pink",
         "users":0,
         "channel_points":0,
         "top_predictors":[
            
         ]
      }
   ],
   "started_at":"2023-12-12T06:49:42.2681038Z"
}
```
## Charity
```json [CharityStarted]
{
  "id": "23f362ba-4a53-40dc-895e-612619d494d2",
  "current_amount": {
    "value": 0,
    "decimal_places": 2,
    "currency": "USD"
  },
  "target_amount": {
    "value": 0,
    "decimal_places": 2,
    "currency": "USD"
  },
  "started_at": "2023-12-11T23:17:52.0356617Z",
  "charity_name": "Test Charity",
  "charity_description": "Test Charity",
  "charity_logo": "Test Charity",
  "charity_website": "Test Charity"
}
```
```json [CharityDonation]
{
  "id": "08d5b644-e12d-4d8b-9ffc-4fc14761b000",
  "campaign_id": "99d206b7-68ed-48bc-a7ce-c020cde2fa63",
  "user_id": "60186332",
  "user_login": "madcapthulhu",
  "user_name": "MadCapthulhu",
  "amount": {
    "value": 0,
    "decimal_places": 2,
    "currency": "USD"
  },
  "charity_name": "Charity Test"
}
```
```json [CharityProgress]
{
  "id": "e309aa6e-6d56-48e0-b8b6-0155c4b7d8d8",
  "current_amount": {
    "value": 0,
    "decimal_places": 2,
    "currency": "USD"
  },
  "target_amount": {
    "value": 0,
    "decimal_places": 2,
    "currency": "USD"
  },
  "charity_name": "Charity Test",
  "charity_description": "Charity Test",
  "charity_logo": "Charity Test",
  "charity_website": "Charity Test"
}
```
```json [CharityCompleted]
{
  "id": "d1b9283d-605a-4bb9-87a8-075b1c9d66ea",
  "current_amount": {
    "value": 0,
    "decimal_places": 2,
    "currency": "USD"
  },
  "target_amount": {
    "value": 0,
    "decimal_places": 2,
    "currency": "USD"
  },
  "stopped_at": "2023-12-11T23:35:57.9694767Z",
  "charity_name": "Charity Test",
  "charity_description": "Charity Test",
  "charity_logo": "Charity Test",
  "charity_website": "Charity Test"
}
```
```json [UserBanned]
{
   "target_user_display": "<banned user's display name>",
   "target_user_id": "00000000",
   "target_user_login": "<banned username>",
   "created_at": "2023-12-12T00:59:55.9987566+01:00",
   "created_by_user_id": "00000000",
   "created_by": "<moderator's username>",
   "duration": 0,
   "reason": "Test",
   "isTest": true
}
```
```json [UserTimedOut]
{
  "target_user_display": "<timed out display name>",
  "target_user_id": "00000000",
  "target_user_login": "<timed out username>",
  "created_at": "2023-12-12T01:09:59.4742762+01:00",
  "created_by_user_id": "00000000",
  "created_by": "<moderator's username>",
  "duration": 10,
  "reason": "test",
  "isTest": true
}
```
```json [ShoutoutReceived]
{
  "from_broadcaster_user_id": "00000000",
  "from_broadcaster_user_login": "<username>",
  "from_broadcaster_user_name": "<display name>",
  "viewer_count": 1,
  "started_at": "2023-12-12T00:40:13.156235Z"
}
```
```json [Announcement]
{
  "subscriber": false,
  "message": "test",
  "emotes": [],
  "badges": [],
  "monthsSubscribed": 0,
  "announcementColor": "green", /* Blue - Green - Orange - Purple */
  "userId": "140918389",
  "userName": "<username>",
  "displayName": "<display name>",
  "role": 0, /* 1 - Viewer, 2 - VIP, 3 - Moderator, 4 - Broadcaster  */
  "isTest": true
}
```


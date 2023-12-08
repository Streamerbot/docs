# Present Viewers
Trovo present viewers trigger.

## Details
The present viewers trigger runs every 1-10 minutes, by default every 5 minutes. It'll give a list of all the users in your stream, this data can be only used in C#.

::list
- Trovo Service: `Chat Client`
::

## Variables
:variables-description
Name | Description
----:|:------------
`title` | The stream title
`audienceType` | The current audience type
`categoryId` | The current category ID
`categoryName` | The current category name
`viewerCount` | The current viewer count
`subscribers` | The amount of subscribers
`followers` | The amount of followers
`startedAt` | The epoch time the stream has stated
`isLive` | Boolean for current streaming status <br> `True`/`False` 
`users` | A C# Dictionary list of usernames present in chat <br> Each user present will get [the following data](#users-dictionary)

### users Dictionary
Name | Description | Example
----:|:------------|:--------
`id` | The user id of the user | `trovo_678296378`
`userName` | The user name of the user | `trovouser123`
`display` | The display name of this user | `TrovoUser123`
`role` | The role of the user | 1=`Viewer`, 2=`VIP`, 3=`Moderator`, 4=`Broadcaster`
`isSubscribed` | Boolean value indicating user's subscription status | `True`/`False`
`isModerator` | Boolean value indicating if the user is a moderator | `True`/`False`

:wip
* Role in users dictionary
---
version: 0.1.17
---

# Stream Online
This triggers when the stream has started on your broadcaster account.

## Details
::list
- Twitch Service: `EventSub`
::

## Variables
:variables-description
Name | Description
----:|:------------
`startedAt` | The date and time that the stream went online
`game` | The category name
`gameId` | The category id
`tagCount` | The number of tags
`tag#` | Each individual tag
`tags` | A `List<string>()` object for use in C#
`tagsDelimited` | A comma delimited string of the tags

::callout{color=amber icon=i-mdi-lightbulb}
Change the `#` to a number from 0 to the end of the tags. So e.g. `%tag0%`, `%tag1%`, `%tag2%`
::
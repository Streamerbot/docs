---
title: Version 0.0.33
description:
published: true
date: 2023-06-11T18:23:03.418Z
tags:
editor: markdown
dateCreated: 2021-08-25T21:35:19.768Z
---

* Misc fixes
* Was missing a scope for subscription information (will likely cause a re-authentication)
* Logging was not set correctly on startup, and don't forget you can increase logging level
{.changelog-fixes}

<span></span>

* Timed actions are now in seconds (I did no conversions, so be sure to update your timers!)
* First word event now includes raw input in arguments
{.changelog-updates}

<span></span>

* Add new File Watcher event
* Add new raid start/send events
* Add option to use system default sound when device can't be found, or do nothing
* Add new sub-action, set timer state (enable/disable timers)
* Add option for timed action to be repeatable or run-once
{.changelog-new}

## File Watcher Event
You can now monitor a file for changes, creation and deletion.

When a file is changed or created, its contents are also loaded into the arguments, add a new file watcher to see all the available arguments.

**Sample Import for File Watcher Actions:**
```
TlM0RR+LCAAAAAAABADtVk2P3DYMvQfIf3AHCNAAS0CS9ZmegjRNCxQ5BeihyIGiqGQAr2fq8aS7CPLfK9u7mY2zu+1MOpOg6MmWKIrkI/nE9w8fVNXiHXeb5apdPKnk2bjR4jmX1eKnZcO/YU9vuaueX+D5uuHFdAKpLxqbcuj3YV1V76dPES3ToCprVzNjDRQpg45M4LVzkEzg4KnWjtV016j0x5a3g8l22zS73Vv8eMWbvvr+2Vts33B6fOOGDtu0On86+lV0MjYb3klp1dK267jtP5d9Fssn8YxH3mG3xNjwyyuH+HzdX+6Mj2dWa+7wyro4m6k3Y3SLvtvyTG2y/ssImpaGnA8aSHIAXWeGoI2FpFKmRAUyxrl67rn7GLX8VDilQuvo2ScHAo0BbbyAiCUVZFBZF33MkWa39pfrwV+pZoG86Vbb9TxNoyRxg5e3SpZt4osBk93uh7NjAz2m+B6kMQYtjDKQpUbQkjPEJGQBxjqnuVbBqf2RRsKYYin6YKwHjd5DyEoDovJsspAhzJ06BtLyBtLXv6/n9f5iMDAW/Q0RYftz6aNmcGmo1Ulwna55jxNZa5xg0Lku5SptAC8CQ44sk+EaydPhPf6CW+6WdLIe7/miv3bkSfWIRop5VdLzaJaydceZi530lGi1Ha2J26qh5mCNsQSS2IHWCsErFUFaGbQWXAsMd1TDkdrumMXgTHYx1YVWVCwdRWghWFWX2kjGGp1FtgcT/tei+V0NHEBBV2/UPSS03xs5qf89CXkUhdRtgqB0oXulAkSpMhC5SGySVvEUJHQQ3X8Z4B1jfy/g+xHWPwWcYkjBOA0OrQadZAJUBoEte4+5pMHe1efHYv3TAP4jN/w1AA8hEwlSkK23pcJDDZhqASFmKhOUZRXECQBXJ2LW/abCA0fps+r5MGp9A6/tD5MnZXMc/sr612XLm7JuyvfZ8OL+d17kOxv1Jj7VclONWHx3YNxYi2hFrkEkP8RdhtNYKAuSdJwVOyNx3sVHiPtUY+l+s/3B/fJy1f/fM99uz/yJm6otKfqixnGp9iKyB4NGlEdMRiiDmQWFknVW6Ex9guD/9cYZPtOpqfontYcPPvwFvwZiKRASAAA=
```

## Raid Start/Send Event
You can now aadd actions to when you start a raid, and when you send a raid.

There's probably more I forgot to write down, and all those new typos for Krayn to.
---
title: Version 0.1.7
description: Released 2022-01-16
published: true
date: 2023-04-28T18:12:45.800Z
tags: 
editor: markdown
dateCreated: 2023-04-28T18:12:43.585Z
---

* Get/Set Action State sub-action had incorrect title in dialog
* OBS Set Replay Buffer state was using incorrect data, should work correctly now
* Fix typo in Logic if
* Voice control commands will delete correctly now if it's not active
* Set Media Source should set a local file correctly now
* /me no longer causes issues with Twitch emote parsing
* 7TV DNS resolution failures should no longer cause a startup crash
* [GetClips should be working correctly now when specifying date ranges](#getclips-api)
{.changelog-fixes}

* Command cooldown action now applies to any command type, instead of exact/start only
* FetchURL is now type aware, the variable the result is put into will attempt to match its contents to the proper type, this is an interm update until more can be done.  If you want explicit control, use C# to fetch data
* Updated Newtonsoft.Json library to 13.0.1
{.changelog-updates}

## GetClips API

> With the addition to being able to specify date ranges/counts for clips, they are no longer returned in newest to oldest, they are returned oldest to newest, as this is how the Twitch API returns the data. There is no mechanism in the API to change the sort order.  Wiki entries will be updated to indicate this
{.is-info}
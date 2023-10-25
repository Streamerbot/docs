---
title: Shop Order
description: Ko-Fi Triggers Reference
published: true
date: 2023-03-16T11:08:54.770Z
tags: 
editor: markdown
dateCreated: 2023-03-15T21:12:48.715Z
---

## Overview
This triggers when you get a shop order via Ko-Fi.

For a detailed guide about Ko-Fi see [this page](/Integrations/Ko-Fi).

## Variables
Name | Description
----:|:------------
`messageId` | Kofi's internal ID
`timestamp` | Timestamp of when the event occured
`from` | Username of who triggered the event
`isPublic` | Whether or not the message should be shared publicly `True`/`False`
`message` | Message the user left
`amount` | The order amount
`currency` | The currency of the order
`itemCount` | The currency of the donation
`item#` | The id of the item purchased, where # is the index of the item
{.vars-table}

> Change the `#` to a number from 0 to the end of the items. So e.g. `%item0%`, `%item1%`, `%item2%`
{.is-info}

---

- [<i class="mdi mdi-chevron-left"></i>**Ko-Fi Triggers Reference *Go Back***](/Triggers/Ko-Fi)
- [<i class="mdi mdi-account primary--text"></i> **Subscription *Next Up***](/Triggers/Ko-Fi/Subscription)
{.btn-grid .my-5}
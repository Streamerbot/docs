---
title: Commission
description: Ko-Fi Triggers Reference
published: true
date: 2023-03-16T11:07:50.482Z
tags: 
editor: markdown
dateCreated: 2023-03-15T21:06:13.859Z
---

## Overview
This triggers when you get a commission via Ko-Fi.

For a detailed guide about Ko-Fi see [this page](/Integrations/Ko-Fi).

## Variables
Name | Description
----:|:------------
`messageId` | Kofi's internal ID
`timestamp` | Timestamp of when the event occured
`from` | Username of who triggered the event
`isPublic` | Whether or not the message should be shared publicly `True`/`False`
`message` | Message the user left
`amount` | The commission amount
`currency` | The currency of the commission
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Ko-Fi Triggers Reference *Go Back***](/Triggers/Ko-Fi)
- [<i class="mdi mdi-cash primary--text"></i> **Donation *Next Up***](/Triggers/Ko-Fi/Donation)
{.btn-grid .my-5}
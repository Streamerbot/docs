---
title: Donation
description: Ko-Fi Triggers Reference
published: true
date: 2023-03-16T11:08:15.123Z
tags: 
editor: markdown
dateCreated: 2023-03-15T21:07:49.317Z
---

## Overview
This triggers when you get a donation via Ko-Fi.

For a detailed guide about Ko-Fi see [this page](/Integrations/Ko-Fi).

## Variables
Name | Description
----:|:------------
`messageId` | Kofi's internal ID
`timestamp` | Timestamp of when the event occured
`from` | Username of who triggered the event
`isPublic` | Whether or not the message should be shared publicly `True`/`False`
`message` | Message the user left
`amount` | The donation amount
`currency` | The currency of the donation
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Ko-Fi Triggers Reference *Go Back***](/Triggers/Ko-Fi)
- [<i class="mdi mdi-account-reactivate primary--text"></i> **Resubscription *Next Up***](/Triggers/Ko-Fi/Resubscription)
{.btn-grid .my-5}
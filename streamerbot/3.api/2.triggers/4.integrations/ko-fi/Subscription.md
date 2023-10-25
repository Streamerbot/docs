---
title: Subscription
description: Ko-Fi Triggers Reference
published: true
date: 2023-03-16T11:07:32.369Z
tags: 
editor: markdown
dateCreated: 2023-03-15T21:09:58.598Z
---

## Overview
This triggers when you get a subscription via Ko-Fi.

For a detailed guide about Ko-Fi see [this page](/Integrations/Ko-Fi).

## Variables
Name | Description
----:|:------------
`messageId` | Kofi's internal ID
`timestamp` | Timestamp of when the event occured
`from` | Username of who triggered the event
`isPublic` | Whether or not the message should be shared publicly `True`/`False`
`message` | Message the user left
`amount` | The subscription amount
`currency` | The currency of the subscription
`tier` | The tier of the subscription
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Ko-Fi Triggers Reference *Go Back***](/Triggers/Ko-Fi)
- [<i class="mdi mdi-contactless-payment-circle primary--text"></i> **Commission *Next Up***](/Triggers/Ko-Fi/Commission)
{.btn-grid .my-5}
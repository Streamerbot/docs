---
title: Pledge Deleted
description: Patreon Triggers Reference
published: true
date: 2023-03-17T21:19:35.997Z
tags: 
editor: markdown
dateCreated: 2023-03-15T20:46:44.819Z
---

## Overview
This triggers when a pledge is deleted on Patreon.

For a detailed guide about Patreon see [this page](/Integrations/Patreon).

## Variables
Name | Description
----:|:------------
`id` | The ID of this event.
`attributes.campaign_lifetime_support_cents` | All the money that the campaign has raised (in U.S. cents).
`attributes.currently_entitled_amount_cents` | All the money that the pledge has raised (in U.S. cents).
`attributes.email` | The full email address of the plegder.
`attributes.full_name` | The full name of the plegder. <br> `John Doe`
`attributes.is_follower` | If the user is a follower. <br> `True`/`False`
`attributes.last_charge_date` | The date the pledge was created. <br> `2022-07-27T15:11:03.000+00:00`
`attributes.last_charge_status` | The charge status of the pledge. <br> `True`/`False`
`attributes.lifetime_support_cents` | The amount of cents the user has given (in U.S. cents).
`attributes.next_charge_date` | Then next charge date of the user.
`attributes.note` | The note that the user has given.
`attributes.patron_status` | If the user is subscribed to your patreon.
`attributes.pledge_cadence` | Number of months between charges.
`attributes.pledge_relationship_start` | The date that the user subsribed to your patron.
`attributes.will_pay_amount_cents` | The amount of cents the user has given (in U.S. cents).
`user.Attributes.about` | The about text of the user.
`user.Attributes.created` | When the account of the user was created.
`user.Attributes.full_name` | The full name of the user. <br> `John Doe`
`user.Attributes.first_name` | The first name of the user. <br> `John`
`user.Attributes.last_name` | The last name of the user. <br> `Doe`
`user.Attributes.hide_pledges` | If the user has it's pledges hidden.
`user.Attributes.image_url` | The profile image of the patron.
`user.Attributes.is_creator` | If the user is a creator. <br> `True`/`False`
`user.Attributes.like_count` | The like count of the user.
`user.Attributes.social_connections.deviantart` | The link to the user's DeviantArt, returns null if not filled out.
`user.Attributes.social_connections.discord` | The link to the user's Discord, returns null if not filled out.
`user.Attributes.social_connections.facebook` | The link to the user's Facebook, returns null if not filled out.
`user.Attributes.social_connections.google` | The link to the user's Googke, returns null if not filled out.
`user.Attributes.social_connections.instagram.url` | The link to the user's Instagram, returns null if not filled out.
`user.Attributes.social_connections.instagram.user_id` | The user's Instagram ID, returns null if not filled out.
`user.Attributes.social_connections.reddit` | The link to the user's Reddit, returns null if not filled out.
`user.Attributes.social_connections.spotify` | The link to the user's Spotify, returns null if not filled out.
`user.Attributes.social_connections.twitch` | The link to the user's Twitch, returns null if not filled out.
`user.Attributes.social_connections.twitter.url` | The link to the user's Twitter, returns null if not filled out.
`user.Attributes.social_connections.twitter.user_id` | The user's Twitter ID, returns null if not filled out.
`user.Attributes.social_connections.vimeo` | The link to the user's Vimeo, returns null if not filled out.
`user.Attributes.social_connections.youtube.url` | The link to the user's YouTube, returns null if not filled out.
`user.Attributes.social_connections.youtube.user_id` | The user's YouTube ID, returns null if not filled out.
`user.Attributes.thumb_url` | The user's thumbnail URL.
`user.Attributes.url` | The user's profile URL.
`user.Attributes.vanity` | The public "username" of the user. patreon.com/ goes to this user's creator page. For non-creator users it might be null.
`user.id` | The user's ID.
`user.type` | The user's type. <br> `user`
`entitledTiers[#].Attributes.title` | The title of this tier.
`entitledTiers[#].Attributes.description` | The description of this tier.
`entitledTiers[#].Attributes.amount_cents` | Monetary amount associated with this tier (in U.S. cents).
`entitledTiers[#].Attributes.created_at` | When this tier was created.
`entitledTiers[#].Attributes.discord_role_ids` | The discord role IDs granted by this tier. Can be null.
`entitledTiers[#].Attributes.edited_at` | When this tier was last edited.
`entitledTiers[#].Attributes.image_url` | The image URL of this tier. 
`entitledTiers[#].Attributes.patron_count` | The amount of patron that have subscribed to this tier.
`entitledTiers[#].Attributes.post_count` | The amount of posts that this tier can see.
`entitledTiers[#].Attributes.published` | If this tier is published <br> `True`/`False`.
`entitledTiers[#].Attributes.published_at` | When this tier was published.
`entitledTiers[#].Attributes.remaining` | How much remaining users this tier has. 
`entitledTiers[#].Attributes.requires_shipping` | If this tier requires shipping <br> `True`/`False`.
`entitledTiers[#].Attributes.unpublished_at` | When this tier was unpublished.
`entitledTiers[#].Attributes.url` | The URL of this tier.
`entitledTiers[#].Attributes.user_limit` | The user limit of this tier.
`entitledTiers[#].id` | The ID of this tier.
`entitledTiers[#].type` | The type of this tier.
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Patreon Triggers Reference *Go Back***](/Triggers/Patreon)
- [<i class="mdi mdi-account-plus" style="color: #ff424e;"></i> **Follow Created *Next Up***](/Triggers/Patreon/Follow-Created)
{.btn-grid .my-5}
---
title: Follow Created
description: This event triggers when you get a follow in Patreon.
variables:
- name: id
	type: string
	description: The ID of this event.
  value: 590e8651-d1f1-4e47-abd4-d1ffdfcbbf49
- name: attributes.campaign_lifetime_support_cents
	type: number
	description: All the money that the campaign has raised (in U.S. cents).
  value: 0
- name: attributes.currently_entitled_amount_cents
	type: number
	description: All the money that the pledge has raised (in U.S. cents).
  value: 0
- name: attributes.email
	type: string
	description: The full email address of the plegder.
  value: JohnDoe@example.com
- name: attributes.full_name
	type: string
	description: The full name of the plegder.
  value: John Doe
- name: attributes.is_follower
	type: boolean
	description: If the user is a follower.
  value: True
- name: attributes.last_charge_date
	type: string
	description: The date the pledge was created.
  value: 01/01/0001 00:00:00
- name: attributes.last_charge_status
	type: string
	description: The charge status of the pledge.
  value: Paid
- name: attributes.lifetime_support_cents
	type: number
	description: The amount of cents the user has given (in U.S. cents).
  value: 0
- name: attributes.next_charge_date
	type: string
	description: Then next charge date of the user.
  value: 01/01/0001 00:00:00
- name: attributes.note
	type: string
	description: The note that the user has given.
  value: Has 5 bucks
- name: attributes.patron_status
	type: string
	description: If the user is subscribed to your patreon.
  value: active_patron
- name: attributes.pledge_cadence
	type: number
	description: Number of months between charges.
  value: 1
- name: attributes.pledge_relationship_start
	type: string
	description: The date that the user subscribed to your patron.
  value: 01/01/0001 00:00:00
- name: attributes.will_pay_amount_cents
	type: number
	description: The amount of cents the user has given (in U.S. cents).
  value: 0
- name: user.Attributes.about
	type: string
	description: The about text of the user.
  value: About me
- name: user.Attributes.created
	type: string
	description: When the account of the user was created.
  value: 01/01/0001 00:00:00
- name: user.Attributes.full_name
	type: string
	description: The full name of the user.
  value: John Doe
- name: user.Attributes.first_name
	type: string
	description: The first name of the user.
  value: John
- name: user.Attributes.last_name
	type: string
	description: The last name of the user.
  value: Doe
- name: user.Attributes.hide_pledges
	type: boolean
	description: If the user has their pledges hidden.
  value: True
- name: user.Attributes.image_url
	type: string
	description: The profile image of the patron.
  value: 
- name: user.Attributes.is_creator
	type: boolean
	description: If the user is a creator.
  value: False
- name: user.Attributes.like_count
	type: number
	description: The like count of the user.
  value: 0
- name: user.Attributes.social_connections.deviantart
	type: string
	description: The link to the user's DeviantArt, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.discord.url
	type: string
	description: The link to the user's Discord, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.discord.user_id
	type: string
	description: The user's Discord ID, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.facebook
	type: string
	description: The link to the user's Facebook, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.google
	type: string
	description: The link to the user's Google, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.instagram
	type: string
	description: The link to the user's Instagram, returns null if not filled out. 
  value:
- name: user.Attributes.social_connections.reddit
	type: string
	description: The link to the user's Reddit, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.spotify
	type: string
	description: The link to the user's Spotify, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.twitch
	type: string
	description: The link to the user's Twitch, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.twitter.url
	type: string
	description: The link to the user's Twitter, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.twitter.user_id
	type: string
	description: The user's Twitter ID, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.vimeo
	type: string
	description: The link to the user's Vimeo, returns null if not filled out.
  value:
- name: user.Attributes.social_connections.youtube
	type: string
	description: The link to the user's YouTube, returns null if not filled out.
  value:
- name: user.Attributes.thumb_url
	type: string
	description: The user's thumbnail URL.
  value:
- name: user.Attributes.url
	type: string
	description: The user's profile URL.
  value:
- name: user.Attributes.vanity
	type: string
	description: The public "username" of the user. patreon.com/ goes to this user's creator page. For non-creator users it might be null.
  value: johndoe
- name: user.id
	type: string
	description: The user's ID.
  value: 12345678
- name: user.type
	type: string
	description: The user's type.
  value: user
- name: entitledTiers[#].Attributes.title
	type: string
	description: The title of this tier.
  value: 
- name: entitledTiers[#].Attributes.description
	type: string
	description: The description of this tier.
  value: 
- name: entitledTiers[#].Attributes.amount_cents
	type: string
	description: Monetary amount associated with this tier (in U.S. cents).
  value: 0
- name: entitledTiers[#].Attributes.created_at
	type: string
	description: When this tier was created.
  value: 01/01/0001 00:00:00
- name: entitledTiers[#].Attributes.discord_role_ids
	type: string
	description: The discord role IDs granted by this tier. Can be null.
  value: 
- name: entitledTiers[#].Attributes.edited_at
	type: string
	description: When this tier was last edited.
  value: 01/01/0001 00:00:00
- name: entitledTiers[#].Attributes.image_url
	type: string
	description: The image URL of this tier.
  value: 
- name: entitledTiers[#].Attributes.patron_count
	type: number
	description: The amount of patron that have subscribed to this tier.
  value: 0
- name: entitledTiers[#].Attributes.post_count
	type: number
	description: The amount of posts that this tier can see.
  value: 0
- name: entitledTiers[#].Attributes.published
	type: boolean
	description: If this tier is published
  value: True
- name: entitledTiers[#].Attributes.published_at
	type: string
	description: When this tier was published.
  value: 01/01/0001 00:00:00
- name: entitledTiers[#].Attributes.remaining
	type: number
	description: How much remaining users this tier has.
  value: 0
- name: entitledTiers[#].Attributes.requires_shipping
	type: boolean
	description: If this tier requires shipping.
  value: False
- name: entitledTiers[#].Attributes.unpublished_at
	type: string
	description: When this tier was unpublished.
  value: 01/01/0001 00:00:00
- name: entitledTiers[#].Attributes.url
	type: string
	description: The URL of this tier.
  value: 
- name: entitledTiers[#].Attributes.user_limit
	type: number
	description: The user limit of this tier.
  value: 0
- name: entitledTiers[#].id
	type: string
	description: The ID of this tier.
  value: 
- name: entitledTiers[#].type
	type: string
	description: The type of this tier.
  value: 
  ---
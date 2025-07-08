---
title: Patreon User Attributes Variables
navigation.title: Patreon User Attributes
variables:
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
---
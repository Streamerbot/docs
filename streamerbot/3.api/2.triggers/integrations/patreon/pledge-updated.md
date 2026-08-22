---
title: Pledge Updated
description: This event triggers when a pledge is updated in Patreon.
variables:
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
  - name: entitledTiers[#].updatedToTier
    type: string
    description: The tier the user has updated to.
    value:
commonVariables:
  - PatreonEventId
  - PatreonUser
  - PatreonUserAttributes
  - PatreonMemberAttributes
---
---
title: Incentive
description: Trigger for a DonorDrive Incentive
version: 0.1.5
variables:
  - name: donorName
    type: string
    description: The name of the donor
  - name: donorAvatarUrl
    type: string
    description: The URL of the donor's avatar
  - name: donorIsAnonymous
    type: boolean
    description: Is the donor anonymous?
    value: True
  - name: recipientName
    type: string
    description: The broadcaster's name used in the DonorDrive
  - name: donorMessage
    type: string
    description: The message of the donor
  - name: donorAmount
    type: number
    description: The amount that the donor has given
    value: 10
  - name: isTeam
    type: boolean
    description: Is this a team?
    value: True
  - name: isParticipant
    type: boolean
    description: Is the user a participant?
    value: True
  - name: profileName
    type: string
    description: The name of the profile
  - name: profileTeamName
    type: string
    description: The name of the profile's team
  - name: eventName
    type: string
    description: The name of the event
  - name: goal
    type: number
    description: The total goal
    value: 200
  - name: raised
    type: number
    description: The total amount of money that has been raised
    value: 100
  - name: isIncentive
    type: boolean
    description: Is the event an incentive?
    value: True
  - name: incentive.id
    type: string
    description: The id of this incentive.
  - name: incentive.isActive
    type: boolean
    description: Is the incentive active? 
    value: True
  - name: incentive.amount
    type: number
    description: The amount of the incentive.
    value: 10
  - name: incentive.description
    type: string
    description: The description of the incentive.
  - name: incentive.image
    type: string
    description: The image for the incentive. Can be an empty string.
  - name: incentive.quantity
    type: number
    description: The quantity of the incentive. Can be -1.
    value: 5
  - name: incentive.quantityClaimed
    type: number
    description: The amount of claimed quantity.
    value: 2
  - name: incentive.links.donate
    type: string
    description: The url of the donate link.
  - name: incentive.startDate
    type: DateTime
    description: The timestamp this incentive starts.
    value: 8/4/2023 10:56:06 AM
  - name: incentive.endDate
    type: DateTime
    description: The timestamp this incentive ends.
    value: 8/4/2023 10:56:06 AM
---

:wip

## Parameters
::field-group
  ::field{name=DonorDrive type=Select required}
    Choose a configured DonorDrive Provider
    - Select `Any` to trigger on any provider
  ::
::
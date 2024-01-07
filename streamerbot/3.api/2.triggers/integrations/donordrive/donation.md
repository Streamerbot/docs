---
title: Donation
description: Trigger for a DonorDrive Donation
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
  - name: donations
    type: array
    description: An array of the donations
  - name: raised
    type: number
    description: The total amount of money that has been raised
    value: 100
---

:wip

## Parameters
::field-group
  ::field{name=DonorDrive type=Select required}
    Choose a configured DonorDrive Provider
    - Select `Any` to trigger on any provider
  ::
::
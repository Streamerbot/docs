---
title: Profile Updated
description: Trigger for when your DonorDrive Profile is Updated
version: 0.1.5
variables:
  - name: name
    type: string
    description: The name of the profile
  - name: teamName
    type: string
    description: The name of the team
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
  - name: isTeam
    type: boolean
    description: Is this profile a team?
    value: True
  - name: isParticipant
    type: boolean
    description: Is the user a participant?
    value: True
---

:wip

## Parameters
::field-group
  ::field{name=DonorDrive type=Select required}
    Choose a configured DonorDrive Provider
    - Select `Any` to trigger on any provider
  ::
::
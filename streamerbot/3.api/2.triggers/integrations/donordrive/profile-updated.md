# Profile Updated
DonorDrive profile updated trigger.

## Details
This event triggers when a profile get updated in DonorDrive.

## Parameters
### `DonorDrive`
Select any or a DonorDrive provider as the source for this donation.

## Variables
:variables-description

Name | Description
----:|:------------
`name` | the name of the profile
`teamName` | The name of the team
`eventName` | The name of the event
`goal` | The total goal
`donations` | An array of the donations
`raised` | The total amount of money that has been raised
`isTeam` | A `True`/`False` response if this is a team
`isParticipant` | A `True`/`False` response if the user is a participant
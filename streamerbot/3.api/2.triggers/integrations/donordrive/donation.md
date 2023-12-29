# Donation
DonorDrive donation trigger.

## Details
This event triggers when you get a donation with DonorDrive.

## Parameters
### `DonorDrive`
Select any or a DonorDrive provider as the source for this donation.

## Variables
:variables-description

Name | Description
----:|:------------
`donorName` | The name of the donor
`donorAvatarUrl` | The URL of the donor's avatar
`donorIsAnonymous` | A `true`/`false` response if the donor is anonymous
`recipientName` | The broadcaster's name used in the DonorDrive
`donorMessage` | The message of the donor
`donorAmount` | The amount that the donor has given
`isTeam` | A `true`/`false` response if this is a team
`isParticipant` | A `true`/`false` response if the user is a participant
`profileName` | The name of the profile
`profileTeamName` | The name of the profile's team
`eventName` | The name of the event
`goal` | The total goal
`donations` | An array of the donations
`raised` | The total amount of money that has been raised
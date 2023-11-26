# Hype Train End
When a hype train ends on your channel.

## Details
::list
- Twitch Service: `EventSub`
::

## Variables
:variables-description
Name | Description
----:|:------------
`level` | The current Hype Train level e.g. `3`
`startedAt` | The time the hype train started e.g. `8/25/2020 8:30:27 PM`
`percent` | The amount of percentage for the current level e.g. `80%`
`percentDecimal` | The amount of decimal percentage for the current level e.g. `0.8`
`contributors` | The amount of contributors of the hype train e.g. `10`
`top.bits.user` | The best cheerer of this hype train display name
`top.bits.userName` | The best cheerer of this hype train login name
`top.bits.userId` | The best cheerer of this hype train user id
`top.bits.total` | The amount of bits from the best cheerer of this hype train
`top.subscription.user` | The most amount of giftsubs given by user in this hype train display name
`top.subscription.userName` | The most amount of giftsubs given by user in this hype train login name
`top.subscription.userId` | The most amount of giftsubs given by user in this hype train user id
`top.subscription.total` | The most amount of giftsubs given by user in this hype train giftsub count
`top.other.user` | The user display name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.userName` | The user login name of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.userId` | The user id of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`top.other.total` | The toal amount of the user that have given the most amount of things that aren't bits/giftsubs this hype train
`id` | The unique hype train id
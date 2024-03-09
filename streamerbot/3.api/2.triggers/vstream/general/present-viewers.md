---
title: Present Viewers
description: Trigger for the VStream present viewers event
variables:
  - name: isLive
    type: bool
    description: Is the channel currently live?
    value: true
  - name: title
    type: string
    description: The current stream title
    value: My Stream
  - name: description
    type: string
    description: The current stream description
    value: Welcome to my stream!
  - name: contentWarning
    type: string
    description:
    value: none
  - name: liveAt
    type: DateTime
    description: The date and time the stream went live
    value: 08/03/2024 11:45:39 PM
  - name: scheduledAt
    type: DateTime
    description: The date and time the stream is scheduled to start
    value: 08/03/2024 11:53:35 PM
  - name: tags
    type: string
    description: Tags for the current stream
    value:
  - name: status
    type: string
    description: The current stream status
    value: live
  - name: type
    type: string
    description: The current stream type
    value: livestream
  - name: vodVisibility
    type: string
    description: VOD visibility
    value: public
  - name: users
    type: Dictionary<VStreamUser>
    description: A C# accessible list of users present in chat
    variables:
      - name: id
	type: string
	description: Unique user ID
	value: chan_01hhaj4h2ee00bzhgd1ceaefa2
      - name: userName
	type: string
	description:  The username of the user
	value: vstreamuser123
      - name: display
	type: string
	description: The display name of the user
	value: VStreamUser123
      - name: role
	type: number
	description: The role of the user<br>1=`Viewer`, 2=`VIP`, 3=`Moderator`, 4=`Broadcaster`
	value: 4
      - name: isSubscribed
	type: bool
	description: Is the user subscribed?
	value: true
      - name: isModerator
	type: bool
	description: Is the user a moderator?
	value: true
---
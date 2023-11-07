---
title: Livestream URL
description: Reference of YouTube Concepts
published: true
date: 2023-03-12T15:17:49.998Z
tags:
editor: markdown
dateCreated: 2023-03-12T15:17:46.679Z
---

## Overview
To get your livestream URL you need to do `https://youtu.be/<broadcast id>` and insert the broadcast id in there. To get the broadcast id, what you can do is set a global variable of `broadcastId` on the [Broadcast Started Event](/Platforms/YouTube/Events/Broadcast-Started). And use that global variable in other actions to use the livestream URL.

To be able to do this I've given an [example import](#example-import) below.

## Example Import
```
TlM0RR+LCAAAAAAABADdVk1v2zAMvQ/of9AM9FYNtmLLdm9psa0Fih36BQxDD7JEZwYUK5OttEHX/z7JThp/JANatDvsksSkSJGPfM95PPiAkLcEXRWq9I4ROWoMJZuDffK+K3NtMkCnquSwqCt0fIwuiiVUtQY2RzeXF14bwHhtE1Q25od7Ruix/bKuQrhMcUBFmArAcR4RHAoicJomgPNkQpM4D0lGSZurCfplwLgKSiPl1golyyS4fLU20LE/cGkEfNFqflZUtdIreyRnsuqc2bT0UT7Xb7REv3f200TMtDKLl6DQRDF5z1bVpSnHJWhWCjWfNlCNvdxmN1pDWY99I3h7EDdHKmU0dx36Rz37kunCofZt3X+mFROcVfW58PonF24LqnqMb+MVtt2iZK6O23XKv6cTkDMj61smx5PsLAZL0xBIFttNoBkOU4hxRnPAlJAk4z4keZANMt9DMfvpUPI/DZqtVwt3V0CCvn0zynERe1aqLbAU8OCu2Vqfjvbhv1z36Z2BBrRSBnFWIlMBOuxgdIiK0jk1ujIZnq7H2r+WK6m0y+TtxCsKOI2zCQ7y0MfhJIpxmuc5Zv6EBNTnIdDJi/Hy/fQtAQs6gG1+3g23+au7olnpuy4JpGSLCkTH2zo3yA+FhaQBJBGLMJlEFIccQpxSkeM8ZxTiJKI04P9EWE42U0ZXNdOWRujz0pL5/1GYjgK8n8zsl7E1vfYnbvchI+GE04Ti2KcBDoMwwAkHjmGSEh7Yz5SFL9cT8l568mb0cF/tyXbHO6E2bD63m7Hz9dwCPhi8v6MsO7d5Udu53VR2goPCnp07y24nExGfAYtyLHxqlSsnVrREQnCQ8lQkCWNCUG8XJwerWpQNKUdknSvRX5xN3+PXvjdE+/w1f1K4UlKo+3K6TdGXFan4hi5Bp/5ZqTScqHrKuTINGfuNrBly6pygd/F44/BHQW44ewPN1ulG9PjUyckquIKyKmqL0zhyJlXG5Om64f7NbdZdntfp28yqWH3dMs/vbvfBh6c/8t2IxrAKAAA=
```

## Actions
Action | Event | Description
------:|:-----:|:-----------
`[Livestream URL] Broadcast Started Event` | YouTube >> Broadcast Started | This saves the broadcast id so you can use it later on in your livestream.
`[Livestream URL] Get Live Stream URL` | Any | Here you can do stuff with the broadcast id, using the `%livestreamUrl%` variable.
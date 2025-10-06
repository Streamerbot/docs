---
title: Version 0.0.37
description: 
published: true
date: 2023-06-11T18:20:05.678Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:35:32.039Z
---

* Fix OBS Recording sub-action, missed a few things in haste
{.changelog-fixes}

<span></span>

* Add new OBS Raw sub-action
{.changelog-new}

## OBS Raw Sub-Action
Send whatever JSON you want to your OBS web socket, it will return back `%obsStatus%` to variables (for now, will merge all variable in, in the future).

This would be a power-user sub-action; At minimum, request-type is a requirement in your JSON. The dialog for adding this sub-action includes a parser so you can visualize the JSON, and using the test button will output the results to the results tab.

This sub-action may change over time.

For information, [https://github.com/Palakis/obs-websocket/blob/4.x-current/docs/generated/protocol.md#requests] are the requests that can be sent.

As a last note, variable replacement is not enabled for this sub-action yet.
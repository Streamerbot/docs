---
title: Version 0.0.39
description: 
published: true
date: 2023-06-11T18:19:17.960Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:35:39.743Z
---

* Update to new twitch library parsing
{.changelog-updates}

<span></span>

* Add capability to listen to whispers, this requires a new authorization scope, so it will invalidate your current login.
* Add new event that can be used when a new quote is added
{.changelog-new}

For Quote Add action, I would recommend importing the sample, and using that for now, it replaces the default hard coded action; I'll reiterate, without this action, it will no longer acknowledge a quote being added (but it will be added)

Sample action import for new quote added action
```
TlM0RR+LCAAAAAAABABtUctugzAQvEfKP1hU3GLJgMGlN05tjz1XPTjeJY1EDDG4ShTl3+uHKhqSE+zO7MxofFmvCEl+0Iz7XicvJNuEhZYHdFPyYfsJG4AkrqWaHG10yKefCbnEj4P24Pmct1nOi4xyoTjlz1LQrapyWlYCUbKMiaKOWuHoaNF6H227bt4+Ng+QkRr6QxNiOEoruxFnVPVaWWNQT/fYXfSb+IEy4ckfJqkd0aQbcvT+5FuOZIuoiQRAIG56SgPyDumcLAgMBlt0/tAo1duQgt0yYktCAGO1UrTKWU05Y4LWKlc047htoZRlIauF9HQefCfZQm9nejssCwwIYCfPD5G9Bjz5aPP2+vf7tSzs1RuE1v5BSuo39xCdTzQZixEIIpEVHzaerVfXX+nScWNlAgAA
```

Sample action import for receiving a whisper
```
TlM0RR+LCAAAAAAABAB9kctuwyAQRfeR8g/IkndBwo/gJLus2n5BF1UXGIbWlY1dHk2iKP9eA63cOFVWMHNm7lyG83KBUPIF2jS9SnYoW4WEYh2MUfL83pgB9J5bjyNjITAjfvExQud4jKgRvolUFIDmBOdAMlxuC4brsuA4q2gNa0kk5VXUCk2fDpwfplzbTtk7DgLXTIm++0nvkGStgYnyXnGnNSh7y278X70hlFg4+sYkdQZ0ij6csciMYqgDxNAhWlqhVLPDkxqcTSdjoX/QIGEcL/ac9y6YINcVcVP1mm9AyApzkVFcyqrGW5oVmOdiA4TKXHKYSdvT4PeSzfTedO+G+RIDEdCy07+kUQKO3tqUvfxeX+f7evADwtL+IM7U4/gPrXdktYMIgkisip8b25aLyzeg5t4IbgIAAA==
```

**A NOTE ABOUT WHISPERS**
Receiving whispers should be fine and reliable; I cannot add the ability to send whispers, the only mechanism that exists is unreliable, and from my previous reading, is not advisable to do it as it's sometimes treated as spam.  To be able to safely send whispers I think requires more from twitch, an exemption or something, I'm not entirely sure, the information is not clear.

## Whisper Event
So, you can bind an action to whispers and have that trigger everytime you receive a whisper.  Commands were also updated to have a source, message, whisper or both.  By default, it will update any existing commands to Message only.  If you have a command that is set to both, or to whisper and gets activated via a whisper, the whisper action will no longer run.

tldr; Commands from whispers will over-rule the whisper action causing it to not fire
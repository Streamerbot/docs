---
description: Create a 30 second Twitch Clip
example: |
    using System;
    using Twitch.Common.Models.Api; //Needed for ClipData Type
    public class CPHInline
    {
        public bool Execute()
        {
            //Create Clip
            ClipData clip = CPH.CreateClip();
            
            //Access created clip data
            //Get clip creator name
            string creatorName = clip.CreatorName;
            //Get clip url
            string url = clip.Url;
            //Get clip game id
            string gameId = clip.GameId;

            return true;
        }
    }
---

::tip
Due to Twitch API restrictions, the generated clip will always be:
- 30 seconds long
- Titled to match your current stream title

To make your own changes to the clip duration or title, you can manually edit the clip later.
::
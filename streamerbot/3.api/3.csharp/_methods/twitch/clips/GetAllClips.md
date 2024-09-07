---
description: Fetch all clips for the connected Twitch Broadcaster. The list is in descending order by view count.
parameters:
  - import: TwitchClipIsFeatured
example: |
    using System;
    using System.Collections.Generic;//Needed for List
    using Twitch.Common.Models.Api; //Needed for ClipData Type
    public class CPHInline
    {
        public bool Execute()
        {
            //Get List of featured clips
            List<ClipData> clipList = CPH.GetAllClips(true);
            
            //Go through clips and write info to logs
            foreach(ClipData clip in clipList)
            {
                //Get id of current clip
                string id = clip.Id;
                //Get url of current clip
                string url = clip.Url;
                //Get title of current clip
                string title = clip.Title;
                //Get view count of current clip
                int viewCount = clip.ViewCount;
        
                CPH.LogInfo($"ViewCount:{viewCount},Title:{title}, Id:{id}, Url:{url}");
            }
            return true;
        }
    }
---

::tip
Clip data is always sorted by view count (descending) due to Twitch API limitations
::

::warning
  A maximum of `1,000` clips can be returned
::
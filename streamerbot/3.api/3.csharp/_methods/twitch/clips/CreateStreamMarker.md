---
description: Create a Stream Marker on Twitch
example: |
    using System; //must also add netstandard.dll in Find References tab
    using Twitch.Common.Models.Api; //Needed for StreamMarker Type
    public class CPHInline
    {
        public bool Execute()
        {
            //Get input from command for marker
            CPH.TryGetArg("rawInput",out string description);

            //Create marker
            StreamMarker markerInfo = CPH.CreateStreamMarker(description);

            //Access stream marker info
            //Get when marker was created
            DateTime createdAt = markerInfo.CreatedAt;
            //Get Marker position in seconds
            int position = markerInfo.Position;
            //Get marker description
            string markerDesc = markerInfo.Description;

            return true;
        }
    }
---
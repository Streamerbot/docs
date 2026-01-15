---
name: CreateClip
title: CreateClip
description: Create a Twitch Clip
parameters:
  - name: title
    type: string
    default: null
    description: If `null`, will match the stream title at the time of creation.
  - name: duration
    type: int
    default: 30
    description: Clip duration in seconds (min. 5, max 60).
example: |
  using System;
  using Twitch.Common.Models.Api; //Needed for ClipData Type
  public class CPHInline
  {
      public bool Execute()
      {
          //Create a 25 second clip titled "Example Title"
          ClipData clip = CPH.CreateClip("Example Title", 25);

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

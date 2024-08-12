---
title: OBS Raw Requests in C#
description: An example how to send OBS Raw requests and work with the responses in C#
author: tawmae
icon: i-mdi-raw
navigation: false
difficulty: 3
---

You are probably already familiar with sending OBS Raw requests with Streamer.bot's [OBS Raw Generator](https://obs-raw.streamer.bot/) or the Raw subaction that you find under `OBS -> Raw`. Sending it vía the subaction then populates variables that you can further use in your action. Sending Raw requests in C# however works a little different.


# Instructions

1. Retrieving the CPH method

   To avoid typing out the entire `CPH.SendObsRaw()` request by hand, we can make use of the **Copy CPH** function of Streamer.Bot's [OBS Raw Generator](https://obs-raw.streamer.bot/).

   ![C# Raw Copy CPH](assets/csharp_obsraw_copycph.png)

   In our example, we want to send a `GetInputSettings` request to get the text of a Text (GDI+) source called **Bitrate Text**. Copying the CPH method leaves us with this in our clipboard:

   ```cs
   CPH.ObsSendRaw("GetInputSettings", "{\"inputName\":\"Bitrate Text\"}", 0);
   ```

2. Creating the C# code

   Now we can paste that method into our C# code.

   ```cs
   using System;

   public class CPHInline
   {
       public bool Execute()
       {
           CPH.ObsSendRaw("GetInputSettings", "{\"inputName\":\"Bitrate Text\"}", 0);

           return true;
       }
   }
   ```

   Running that code will send the request, but we still don't have a way to fetch the response information. By taking a look into the docs for the C# methods, we can see that the request also returns a **string**. So we simply declare a string and have the request as its value.

   :read-more{to="/api/csharp/obs/raw#ObsSendRaw"}

   ```cs
   using System;

   public class CPHInline
   {
       public bool Execute()
       {
           string getInputSettingsResponse = CPH.ObsSendRaw("GetInputSettings", "{\"inputName\":\"Bitrate Text\"}", 0);

           return true;
       }
   }
   ```

3. Parsing the response

   The response we get is actually just plain text in a JSON format. You can check that by logging that info with `CPH.LogInfo(getInputSettingsResponse);` or by using the OBS Raw Generator.

   ```json
   {
     "inputKind": "text_gdiplus_v3",
     "inputSettings": {
       "color": 8388437,
       "font": {
         "face": "Neue Haas Grotesk Text Pro Extr",
         "flags": 0,
         "size": 144,
         "style": "ExtraLight"
       },
       "text": "Current bitrate: 7500"
     }
   }
   ```

   Now we specifically want the `text` and `fontsize` properties from that entire request. To do that, we need to parse the **string** into a **JObject** first. So we add the namespace `using Newtonsoft.Json.Linq;` and use the `JObject.Parse()` method.

   ```cs
   using System;
   using Newtonsoft.Json.Linq;

   public class CPHInline
   {
       public bool Execute()
       {
           string getInputSettingsResponse = CPH.ObsSendRaw("GetInputSettings", "{\"inputName\":\"Bitrate Text\"}", 0);

           JObject inputSettingsJObject = JObject.Parse(getInputSettingsResponse);

           return true;
       }
   }
   ```

4. Getting specific properties

   This now allows us to directly pick the info we want. As seen in the response, the object is called `inputSettings` and the properties `text` and `font` -> `size`.
   
   To get the `text` property, we can just declare a string and parse that property:

   ```cs
   string gdiText = (string)inputSettingsJObject["inputSettings"]["text"];
   ```

   The `size` property is a number and also nested within the `font` property, so we need to adjust that:

   ```cs
   int fontSize = (int)inputSettingsJObject["inputSettings"]["font"]["size"];
   ```

   So the entire code looks like this:

   ```cs
   using System;
   using Newtonsoft.Json.Linq;

   public class CPHInline
   {
       public bool Execute()
       {
           string getInputSettingsResponse = CPH.ObsSendRaw("GetInputSettings", "{\"inputName\":\"Bitrate Text\"}", 0);

           JObject inputSettingsJObject = JObject.Parse(getInputSettingsResponse);

           string gdiText = (string)inputSettingsJObject["inputSettings"]["text"];

           int fontSize = (int)inputSettingsJObject["inputSettings"]["font"]["size"];

           return true;
       }
   }
   ```

5. Checking the response

   To make sure we got that info correctly, we can output both of them into our logs aswell:

   ```cs
   CPH.LogInfo($"GDI Text: {gdiText} // Font Size: {fontSize}");
   ```

   And checking our logs shows that it worked!

   ```
   [2024-08-11 19:13:48.297 INF] GDI Text: Current bitrate: 7500 // Font Size: 144
   ```

6. Using those variables to send another Raw request

   With our newly obtained information, we can use that variables to send another response. Let's say, we have another text source and want to give it the same text and font size as our **Bitrate Text** source. So we paste the setting parameters into the OBS Raw Generator and copy the CPH method:

   ```json
   {
    "font": {
      "size": 144
    },
    "text": "7500"
   }
   ```

   ```cs
   CPH.ObsSendRaw("SetInputSettings", "{\"inputName\":\"Other Textsource\",\"inputSettings\":{\"font\":{\"size\":144},\"text\":\"7500\"},\"overlay\":true}", 0);
   ```

7. Replace variables

   ::note
   **Variables within CPH.ObsSendRaw Requests**
   <br>
   To use variables within the request, we format them like this:
   <br><br>
   `" + variableName + "`
   ::

   ```cs
   using System;
   using Newtonsoft.Json.Linq;

   public class CPHInline
   {
       public bool Execute()
       {
           string getInputSettingsResponse = CPH.ObsSendRaw("GetInputSettings", "{\"inputName\":\"Bitrate Text\"}", 0);

           JObject inputSettingsJObject = JObject.Parse(getInputSettingsResponse);

           string gdiText = (string)inputSettingsJObject["inputSettings"]["text"];

           int fontSize = (int)inputSettingsJObject["inputSettings"]["font"]["size"];

           CPH.ObsSendRaw("SetInputSettings", "{\"inputName\":\"Other Textsource\",\"inputSettings\":{\"font\":{\"size\": " + fontSize + "},\"text\":\" " + gdiText + "\"},\"overlay\":true}", 0);

           return true;
       }
   }
   ```

   ![C# Raw Result](assets/csharp_obsraw_result.gif)

8. Done! You are now able to send an OBS Raw request as well as fetch info from an OBS Raw request in C#!

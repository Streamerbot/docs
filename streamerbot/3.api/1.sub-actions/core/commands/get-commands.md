---
title: Get Commands
description: Fetch a list of all configured commands
variables:
  - name: '<variableName>'
    type: string
    description: Comma-separated string containing all commands matching your specified criteria
    value: '!shoutout,!followage,!ban'
  - name: '<variableName>List'
    type: List
    description: C# List object containing all commands matching your specified criteria
csharpMethods: []
---

This sub-action is useful if you want to output a list of commands to your chat.

:image-preview

## Example Usage
### Import Code
``` [sb-import]
U0JBRR+LCAAAAAAABADdV1lvm1gUfq/U/xDlubZYjG0q9cEmMSGJSbxiM+7D3YyJL8uweKv63+eAV7yMqqrzMpFQzPm+e5bvHODeH58/3d3dL1gUu4F///VO/pIbXC8MomR4bvZc3/VS72i/F8pSWS4hHs5QWbzfsViCAPuR3cCtjzyWUXWW3GmB5yGfxnePK+SFnN0NYuSw7TqgojSZBVFG7iURg3VRGQfJAT6meS+WhbJwACiLSeSGyQ489Rd0U79Bdoifcp5BP7eJUlRIFOW0GCx/bS13eyiHXZr5rsqsJiK1VqpTEZUqVFXhF5ZLtSmrS6IyVTGj+/j5sr9TlrJd7FM78xHmLPOZRCkrICvCU8paUeA9uXESRGsgTRGPC6xrshYCO1GQhhnjKor4Eq1jEOea7wjogXeQ7QIngU/SKGJ+cg1NItdxoFWZkN8LMS8FPhP5mLi5Le9Mte0YoMjNtNtRIJvL+rYd83MhG5xfqrwlOH4QAe6imMVXSslJMxS/s8hz493sXXWUzwapIgELlJaqSFZKldq0WlKFilyqEjJlmJJ6naCLJJfMdWaZjjDQ51iyDrMKRUGUz6FDd7PqzsGbs7WThbJV5vbU/vPLv7UkDtKIsP4unVsNOX32zqSZ1iuySOpySZKmtFQRFbWEJHiA6JRJgsym1ZpQ/R1plAvgIMxvqiL8uiqng3q1D783qVen8A+PqkIrWKGqWEIMC9mo1kuqolZLskqJjGqCwhT5j4/qfz+n+5fiRaQbX4gDPmcsBHEX7Ja0EZsyeOERdvH6ymHt62RiQcLBMp5M2i6JgjiYJmXzsT+ZtCLIahlE82plMllU4MslC7KoTiZeTIKIu7hMoe9Fl9/P4+N1wrSA5tXRkRlijzgDmW+oPkzelsLLue11bi6wvuJjuRtiSdm8zinH3nCNrHbtoROYmt8Ux94qHK+bH1hvbci6+TB4nD1jsGFvAHhsam7DMbTmklrPMaxzxp66wFqzxfThBx11+Ys233Myn/C/sb0eVyGRO3UidyGe4r+7EEMSk7GlzMm6oRrarI1GpvD+ZArE46m9qYTj0bNPxNgdS2qCrVZqP5k5x+BC7XWtDpDON0Z2PdHAtioO1WfcaNkzWD+DOrjxqMywNXDQHnuknGrNh2PcZp9aRtKxTAFZapr70k/ykhq7WrbXPndDFzmRzZktDZz3XsPtHPJrO52RPcP6Lv5Td2E88QXtgw4fccHXTjcXyx3w0fTG1mpj94sciCUcYw3N8cjJ4glv/UHN0OqLvs4TNOo4aNR2zH5jaehQQ6sro1H3A2lLp/2xt0EOwy70dpC+us3nLC8sxc4Y4toj4mDJ9gzot6E/OkRqga2rZHHHI1MksKbQR91eELcRbHObZ/ks39bN0HhYOsc+tVPQRMR+pwac6GU9L9TFYDYP/g61jp0XbXbUXkzCUU9p26A31R3nZd1M7JG5GVuUv85XMLdUQBrEd4/2vtWqvHQufV+Lt51Js9PTlD7EmO9n4OXY29jQnxdUm+dag65BpjOVeAx9S21rOM/7qz9zQzcDyNm3rQ7MWd3piE3jlZuQY9fG8nAAzwrkNtyAtr7dmx3r2PY/zPSz3aaC5UHmf4O0poDXzU2WF8QI7N6xxjxm1s9R3s+CrsfrhP8gOMa8Nbd1vsBeK4aaF9gSZ5DbZtvLPG7V0Izi87r1o+bvhfMYJ/P/shFO+m5iNBSgVw33VWu4bwXdc1//W+2JNxTo6DkFzppag4OWU5jHaefbt4uvSxgx+PSHLr/5eaGMo3UvQdG1HXXOiNGCdVmc8qQfDI8brpvcAuvWtoxVKEIqEUo1IsCOtSLVS1ipw61KpVqlXlNQrfY72wA1+7u1D7i2p/+1nYBU2Akcb66cMvQs2OURhAScozBm9ATfwzuHe/725FZwcdzAnRqXDMcBmbOkx6LF2bnnCGrchfNSEUxcb8/Pj6WfP/38B42DdriRDwAA
```

### C# Code
Since Twitch has a message character limit of 500 and on YouTube it's 200 you may find your commands overtake this amount therefore the code below can help with splitting the list into batches of commands that fit inside the messages.

```cs
using System;
using System.Collections.Generic;

public class CPHInline
{
    public bool Execute()
    {
        List<string> commands = (List<string>)args["commandsList"];//This is when the Variable Name in the Get Commands Sub-Action is `commands`
        string message = "Commands Avaliable to you: ";
        bool bot = false;
        int messageMax = 495; //Limit is 500 on Twitch, 200 on YouTube.. I took a few off as a safety measure.
        for (int i = 0; i < commands.Count; i++)
        {
            if ((commands[i].Length + message.Length) > messageMax)
            {
                CPH.SendAction(message, bot); // This will need to be changed to CPH.SendYouTubeMessage(message, bot); if you wish to send the message to Youtube
                message = "Addional Commands for you: ";
            }

            message += commands[i] + ", ";
        }
        CPH.SendAction(message, bot); // This will need to be changed to CPH.SendYouTubeMessage(message, bot); if you wish to send the message to Youtube
        return true;
    }
}
```

# Speak
Send a message with text-to-speech (TTS) using Speaker.bot

:image-preview

::list{type=warning}
- Check out the [Speaker.bot Integration Guide](/guide/integrations/speakerbot) for information about configuring Speaker.bot
::

## Parameters
### `Voice Alias`
Enter the name of the voice alias to use.

### `Pass Through Bad Word Filter`
Toggle the bad word filter on or off.

### `Silent`
Will play the TTS silently. Can be used with the delay option if you want to wait before the TTS is finished, but don't have the audio.

### `Delay`
With this option the adjacent sub-action will wait for execution till the TTS has finished playing.

### `Message`
Enter the message content to send to Speaker.bot.

## Variables
:variables-description

|         Name | Description                                              |
|-------------:|:---------------------------------------------------------|
|    `success` | If the speak sub-action was successful `True`/`False`    |
| `speechFile` | The speech file or when it doesn't exist `null`          |
|   `duration` | The duration of the speech when the delay option is used |

## C# Usage
:csharp-method
# Fetch URL
Fetch a remote URL and retrieve the response body
:image-preview{width=400}

> This sub-action behaves much like the URL commands in Nightbot and many other bots.

## Parameters
### `URL`
Enter the URL to fetch

### `Variable Name`
Enter the name of the variable you'd like to store to response in

### `Headers`
Modify request headers
::list{type=warning}
- Only add custom headers if you know what you are doing!
::

## Examples
### Current Weather
- `URL`: `https://api.scorpstuff.com/weather.php?units=metric&city=boston,MA`
- `Variable Name`: `currentWeather`

After execution, the `%currentWeather%` variable will be populated with the response body.

::code-group
  ```bash [Example Response]
  Weather for Boston, US: Broken clouds with a temperature of 29.6 C (85.2 F). Wind is blowing from the East at 12.96 kph (8.05 mph) and the humidity is 59%
  ```
::

You can then use your variable in any subsequent sub-actions.

For example, you could then use the [Twitch Send Message to Channel](/api/sub-actions/platforms/twitch/chat/send-message-to-channel) sub-action to send the output back to chat!
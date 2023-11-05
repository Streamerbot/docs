# Take Screenshot
Makes a screenshot from a scene or source
:image-preview

## Parameters
:parameter{name=ObsConnection}

### `Scene`
Select the scene from this dropdown list, you can also manually enter a scene name.

- Type: `String`

### `Source`
Select the source from this dropdown list, you can also manually enter a source name.

- Type: `String`
- *Optional*

### `File Path`
Select the file path for the screenshot

- Type: `File`
### `Quality`
Select the image quality or leave as `Auto`

- Type: `Slider`

## Variables
Name | Description
----:|:------------
`screenshotFile` | The full path to the screenshot that was taken
`filedatetime` | Date Time variable that can be used for file name `yyyyMMdd.hhmmss`

## C# Usage
:csharp-method{name=ObsTakeScreenshot}
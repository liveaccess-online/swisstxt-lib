
# swisstxt-lib

This JavaScript library provides a customizable transcript overlay that can be embedded on any webpage. The button triggers an overlay containing iframe content, which can be configured to display in different languages.

## Embedding the Library

To use the `swisstxt-lib.js` library on your website, simply include the following script tag in your HTML:

```html
<script src="https://liveaccess-online.github.io/swisstxt-lib/swisstxt-lib.min.js" data-identifier="swisstxt-lib"></script>
```

## Configuration Parameters

The library supports several `data-*` attributes that allow you to customize its behavior. Below is a list of configurable parameters:

### `data-identifier` (required)
- **Description**: Uniquely identifies the script element. This must be set to `"swisstxt-lib"` to ensure the script is correctly initialized.
- **Usage**: 
  ```html
  data-identifier="swisstxt-lib"
  ```

### `data-site` (required)
- **Description**: Specifies the base URL for the iframe content. Use `1` for `https://www.liveaccess.online` or `2` for `https://stage.liveaccess.online`.
- **Usage**: 
  ```html
  data-site="1"
  ```

### `data-path` (required)
- **Description**: Defines the path on which the script should be activated. The overlay and button will only be active on this path.
- **Usage**:
  ```html
  data-path="/your-path"
  ```

### `data-room-id` (required)
- **Description**: The ID of the room to display in the iframe. This is required for the script to function correctly.
- **Usage**:
  ```html
  data-room-id="7c1fmu"
  ```

### `data-button-text`
- **Description**: Customizes the text displayed on the main button. Defaults to `"Transcripts"` if not specified.
- **Usage**:
  ```html
  data-button-text="Transcript"
  ```

### `data-color`
- **Description**: Sets the color scheme of the iframe and buttons. Accepts values from `1` to `6`.
- **Usage**:
  ```html
  data-color="3"
  ```

### `data-height`
- **Description**: Defines the height of the overlay in pixels. Defaults to `200px` if not specified.
- **Usage**:
  ```html
  data-height="300"
  ```

### Language Parameters
- **Description**: Specifies the languages available in the iframe. You can include multiple languages by adding the respective `data-*` attributes. Supported languages are `pre`, `en`, `fr`, `it`, `de`.
- **Usage**:
  ```html
  data-en data-fr data-de
  ```

## Fully Configured Example

Here is an example of a fully configured script tag:

```html
<script src="https://liveaccess-online.github.io/swisstxt-lib/swisstxt-lib.min.js" 
    data-identifier="swisstxt-button"
    data-site="1"
    data-path="/your-path"
    data-room-id="7c1fmu"
    data-button-text="Transcript"
    data-color="3"
    data-height="300"
    data-en
    data-fr
    data-de></script>
```

In this example:
- The script is identified as `swisstxt-button`.
- The content is sourced from `https://www.liveaccess.online`.
- The button and overlay are active on the `/your-path` URL.
- The room ID for the iframe is `7c1fmu`.
- The button text is set to `Transcript`.
- The color scheme `3` is used.
- The overlay height is set to `300px`.
- The available languages are English (`en`), French (`fr`), and German (`de`).

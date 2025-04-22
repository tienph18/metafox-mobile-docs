# Alert

Displays a styled alert box containing an HTML message. The appearance (color, icon) depends on the `severity` and `variant`.

## Props

| Name      | Type                                         | Description                                                                 | Required | Default     |
| :-------- | :------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :---------- |
| `message` | `string`                                     | The HTML content to display in the alert.                                   | Yes      |             |
| `variant` | `'standard'`                                 | Controls the overall style variant of the alert.                            | No       | `'standard'`|
| `severity`| `'success' \| 'info' \| 'warning' \| 'error'` | Determines the alert type (info, success, warning, error), affecting color and icon. | No       | `'info'`    |
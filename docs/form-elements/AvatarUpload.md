# AvatarUpload

A form element that allows users to select and upload an avatar image, displaying a preview. It integrates with the device's image picker and handles basic validation display.

## Props

| Name             | Type                    | Description                                                      | Required | Default     |
| :--------------- | :---------------------- | :--------------------------------------------------------------- | :------- | :---------- |
| `size`           | `string`                | Size of the avatar preview (e.g., 'small', 'medium', 'xxlarge'). | No       | `'xxlarge'` |
| `circle`         | `boolean`               | Renders the avatar preview as a circle.                          | No       | `true`      |
| `margin`         | `keyof typeof SizeEnum` | Margin around the control.                                       | No       | `'none'`    |
| `paddingBottom`  | `keyof typeof SizeEnum` | Bottom padding for the control.                                  | No       | `undefined` |
| `fullWidth`      | `boolean`               | Makes the control span the full width of its container.          | No       | `false`     |
| `required`       | `boolean`               | Marks the field as required within the config context.           | No       | `false`     |
| `variant`        | `Variant`               | Visual style variant of the form control.                        | No       | `undefined` |
| `spaceWidth`     | `number`              | Width of the space around the avatar image.                      | No       | `undefined` |
| `spaceColor`     | `string`              | Color of the space around the avatar image.                      | No       | `undefined` |
| `borderColor`    | `string`              | Color of the border around the avatar image.                     | No       | `undefined` |
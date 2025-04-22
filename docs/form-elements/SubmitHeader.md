# SubmitHeader

This element renders a submit button, typically placed within a form's header area, wrapped in a `FormControl` for layout control. Clicking the button triggers the form submission process.

## Props

| Name          | Type                               | Description                                  | Required | Default    |
| :------------ | :--------------------------------- | :------------------------------------------- | :------- | :--------- |
| `label`       | `string`                           | The text displayed on the button.            | Yes      |            |
| `icon`        | `string`                           | Icon name to display on the button.          | No       |            |
| `color`       | `string`                           | Button color (e.g., 'primary', 'secondary'). | No       |            |
| `size`        | `'small' \| 'medium' \| 'large'`   | Button size.                                 | No       |            |
| `fontWeight`  | `string`                           | Button text font weight.                     | No       |            |
| `textTransform` | `string`                           | Button text transformation (e.g., 'uppercase'). | No       |            |
| `transparent` | `boolean`                          | Makes the button background transparent.     | No       | `false`    |
| `outline`     | `boolean`                          | Applies an outline style to the button.      | No       | `false`    |
| `fullWidth`   | `boolean`                          | If true, the surrounding control takes full width. | No       | `false`    |
| `margin`      | `'none' \| 'dense' \| 'normal'`    | Margin for the surrounding control.          | No       |            |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'`    | Padding bottom for the surrounding control.  | No       | `'normal'` |
| `variant`     | `'standard' \| 'outlined' \| 'filled'` | Variant style for the surrounding control.   | No       | `'standard'`|
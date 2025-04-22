# Submit

A button element used to trigger form submission. It integrates with Formik to handle the submit action and can be configured with various visual styles and behaviors.

## Props

| Name                 | Type                                                              | Description                                                                                   | Required | Default      |
| :------------------- | :---------------------------------------------------------------- | :-------------------------------------------------------------------------------------------- | :------- | :----------- |
| `label`              | `string`                                                          | The text displayed on the button.                                                             | Yes      |              |
| `icon`               | `string`                                                          | Name of the icon to display on the button.                                                    | No       |              |
| `fullWidth`          | `boolean`                                                         | If true, the button takes up the full width of its container.                                 | No       | `false`      |
| `margin`             | `'none' \| 'dense' \| 'normal'`                                   | Controls the margin around the button's container.                                            | No       | `'normal'`   |
| `paddingBottom`      | `'none' \| 'dense' \| 'normal'`                                   | Controls the bottom padding of the button's container.                                        | No       | `'normal'`   |
| `variant`            | `'standard' \| 'outlined' \| 'contained'`                         | The visual style variant of the button's container.                                           | No       | `'standard'` |
| `color`              | `'primary' \| 'secondary' \| 'error' \| 'warning' \| 'info' \| 'success' \| 'inherit' \| string` | The color of the button. Defaults to 'gray' when disabled.                                | No       | `'primary'`  |
| `size`               | `'small' \| 'medium' \| 'large' \| 'string'`                      | The size of the button. Note: The component internally uses 'normal'.                         | No       | `'medium'`   |
| `fontWeight`         | `'light' \| 'regular' \| 'medium' \| 'bold'`                      | The font weight of the button text.                                                           | No       |              |
| `textTransform`      | `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'`            | Controls the text transformation (e.g., uppercase).                                           | No       |              |
| `round`              | `boolean`                                                         | If true, makes the button round (intended for icon buttons).                                  | No       | `false`      |
| `first`              | `boolean`                                                         | Style adjustment if it's the first element in a group.                                        | No       | `false`      |
| `disabled`           | `boolean`                                                         | Disables the button. Note: The component also has internal disable logic (`disableWhenClean`). | No       | `false`      |
| `testID`             | `string`                                                          | Test identifier for automation.                                                               | No       |              |
| `transparent`        | `boolean`                                                         | Makes the button background transparent.                                                      | No       | `false`      |
| `outline`            | `boolean`                                                         | Applies an outline style to the button.                                                       | No       | `false`      |
| `disableWhenClean`   | `boolean`                                                         | If true, the button is disabled when the form is pristine (no changes made).                  | No       | `false`      |
| `style`              | `object`                                                          | Custom styles to apply to the FormControl container.                                          | No       |              |
| `customAction`       | `{ type: string; payload?: any }`                                 | Dispatches a custom Redux action when the button is clicked after submitting the form.        | No       |              |
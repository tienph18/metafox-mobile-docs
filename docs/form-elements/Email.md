# Email

An input field specifically designed for entering email addresses. It renders a standard text input configured for email entry (e.g., `keyboardType='email-address'`, `autoCapitalize='none'`). This element is based on the `Text` form element.

## Props

The component accepts standard form element props (`name`, `config`, `disabled`, `required`, etc.). The primary configuration is done via the `config` object:

| Name                  | Type                                                         | Description                                                                                   | Required | Default         |
| :-------------------- | :----------------------------------------------------------- | :-------------------------------------------------------------------------------------------- | :------- | :-------------- |
| `label`               | `string`                                                     | The label displayed above the input field.                                                    | No       | `undefined`     |
| `placeholder`         | `string`                                                     | Placeholder text shown when the input is empty.                                               | No       | `undefined`     |
| `description`         | `string`                                                     | Additional helper text displayed below the input field.                                       | No       | `undefined`     |
| `required`            | `boolean`                                                    | Whether the field must be filled.                                                             | No       | `false`         |
| `disabled`            | `boolean`                                                    | If `true`, the input field is disabled and cannot be interacted with.                         | No       | `false`         |
| `variant`             | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'` | The visual style of the input field.                                                          | No       | `'standard'`    |
| `margin`              | `'normal'`, `'dense'`, `'none'`                              | Margin applied around the form control.                                                       | No       | `'normal'`      |
| `fullWidth`           | `boolean`                                                    | If `true`, the input field takes up the full width of its container.                          | No       | `false`         |
| `maxLength`           | `number`                                                     | Maximum number of characters allowed in the input.                                            | No       | `undefined`     |
| `autoFocus`           | `boolean`                                                    | If `true`, the input field automatically gains focus when mounted.                            | No       | `false`         |
| `validateAction`      | `string`                                                     | Name of a registered action for backend validation on blur.                                   | No       | `undefined`     |
| `keyboardType`        | `string`                                                     | Determines which keyboard to open (e.g., 'numeric', 'email-address'). For Email, defaults to 'email-address'. | No       | `'email-address'` |
| `autoCapitalize`      | `'none'`, `'sentences'`, `'words'`, `'characters'`           | How to automatically capitalize text. For Email, defaults to 'none'.                          | No       | `'none'`        |
| `returnKeyType`       | `string`                                                     | Determines how the return key should look.                                                    | No       | `'default'`     |
| `textContentType`     | `string`                                                     | Give the keyboard and the system information about the expected semantic meaning for the content. For Email, defaults to 'emailAddress'. | No       | `'emailAddress'` |
| `clearButtonMode`     | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | When to display the clear text button (iOS only).                                             | No       | `'never'`       |
| `...rest`             | `TextInputProps`                                             | Other standard React Native `TextInput` props are accepted.                                   | No       | `undefined`     |

*Note: This element inherits most props from the base `Text` element.*
# question

This element renders a standard text input field. It is an alias for the `Text` element (`form.element.Text`).

## Props

| Name                  | Type                                                     | Description                                                                 | Required | Default         |
| --------------------- | -------------------------------------------------------- | --------------------------------------------------------------------------- | -------- | --------------- |
| `label`               | `string`                                                 | The label displayed for the input field.                                    | No       |                 |
| `placeholder`         | `string`                                                 | The placeholder text displayed when the input is empty.                     | No       |                 |
| `description`         | `string`                                                 | A description displayed below the input field.                              | No       |                 |
| `contextualDescription`| `string`                                                 | Additional description shown below the input, often used for dynamic info. | No       |                 |
| `variant`             | `'standard'`, `'outlined'`, `'filled'`, `'livestream'` etc. | The visual style variant of the input field.                                | No       | `'standard'`    |
| `fullWidth`           | `boolean`                                                | If `true`, the input field takes up the full width of its container.        | No       | `false`         |
| `margin`              | `'normal'`, `'dense'`, `'none'` etc.                     | The margin applied around the form control.                                 | No       | `'normal'`      |
| `paddingBottom`       | `'normal'`, `'dense'`, `'none'` etc.                     | The bottom padding applied.                                                 | No       |                 |
| `required`            | `boolean`                                                | Whether the field is required (visual indicator, validation handled by form). | No       | `false`         |
| `disabled`            | `boolean`                                                | If `true`, the input field is disabled and cannot be interacted with.       | No       | `false`         |
| `editable`            | `boolean`                                                | If `false`, the text field value cannot be changed.                         | No       | `true`          |
| `multiline`           | `boolean`                                                | If `true`, allows multiple lines of text input.                             | No       | `false`         |
| `minHeight`           | `number`                                                 | Minimum height for the input field, useful with `multiline`.                | No       |                 |
| `maxLength`           | `number`                                                 | The maximum number of characters allowed in the input field.                | No       |                 |
| `autoCorrect`         | `boolean`                                                | Controls whether autocorrection should be enabled.                          | No       | `true`          |
| `autoCapitalize`      | `'none'`, `'sentences'`, `'words'`, `'characters'`       | Controls how text input is automatically capitalized.                       | No       | `'sentences'`   |
| `autoFocus`           | `boolean`                                                | If `true`, the input field automatically gains focus when mounted.          | No       | `false`         |
| `keyboardType`        | `string`                                                 | Specifies the type of keyboard to display (e.g., 'numeric', 'email-address'). | No       | `'default'`     |
| `returnKeyType`       | `string`                                                 | Specifies the appearance of the return key (e.g., 'done', 'next').          | No       | `'done'`        |
| `secureTextEntry`     | `boolean`                                                | If `true`, masks the text entered (for passwords).                          | No       | `false`         |
| `clearButtonMode`     | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls when the standard clear button appears in the text field (iOS only). | No       | `'never'`       |
| `validateAction`      | `string`                                                 | Name of a resource action used for asynchronous backend validation on blur. | No       |                 |
| `findReplace`         | `{ find: string, replace: string }`                      | Configuration to display a transformed version of the input (e.g., slug).   | No       |                 |
| `hasQRScanner`        | `boolean`                                                | If `true`, displays a QR code scanner icon button.                          | No       | `false`         |
| `qrScannerParamName`  | `string`                                                 | The URL query parameter name to extract when using the QR scanner.          | No       | `'invite_code'` |
| `hasCopy`             | `boolean`                                                | If `true`, displays a copy-to-clipboard icon button.                        | No       | `false`         |
| `backgroundColor`     | `string`                                                 | Sets a custom background color for the input field.                         | No       |                 |

*Note: This component inherits standard `TextInput` props. Only the most common and element-specific configuration props are listed here.*
# input

A standard text input field allowing users to enter text. It wraps the `TextField` component, providing various configurations for appearance, behavior, validation, and integration with features like QR scanning and copy-to-clipboard.

## Props

| Name                 | Type                                                     | Description                                                                      | Required | Default         |
| :------------------- | :------------------------------------------------------- | :------------------------------------------------------------------------------- | :------- | :-------------- |
| `label`              | `string`                                                 | The label displayed for the input field.                                         | No       |                 |
| `placeholder`        | `string`                                                 | Text displayed when the input is empty.                                          | No       |                 |
| `description`        | `string`                                                 | Help text displayed below the input.                                             | No       |                 |
| `variant`            | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'`, `'livestream'` | Visual style of the input field.                                                 | No       | `'standard'`    |
| `fullWidth`          | `boolean`                                                | If true, the input takes up the full width of its container.                     | No       | `false`         |
| `margin`             | `'none'`, `'dense'`, `'normal'`                          | Margin size around the input field.                                              | No       | `'normal'`      |
| `paddingBottom`      | `'none'`, `'dense'`, `'normal'`                          | Padding size below the input.                                                    | No       | `'normal'`      |
| `required`           | `boolean`                                                | Whether the field is required (client-side).                                     | No       | `false`         |
| `disabled`           | `boolean`                                                | If true, the input is disabled and not editable.                                 | No       | `false`         |
| `editable`           | `boolean`                                                | If false, the text is not editable (overridden by `disabled`).                   | No       | `true`          |
| `multiline`          | `boolean`                                                | If true, the input can span multiple lines.                                      | No       | `false`         |
| `minHeight`          | `number`                                                 | Minimum height for the input, useful for multiline inputs.                       | No       |                 |
| `maxLength`          | `number`                                                 | Maximum number of characters allowed.                                            | No       |                 |
| `autoFocus`          | `boolean`                                                | If true, the input focuses automatically on mount.                               | No       | `false`         |
| `autoCorrect`        | `boolean`                                                | Enable/disable auto-correction.                                                  | No       | `true`          |
| `autoCapitalize`     | `'none'`, `'sentences'`, `'words'`, `'characters'`       | Auto-capitalization behavior.                                                    | No       | `'sentences'`   |
| `clearButtonMode`    | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls when the clear button appears (iOS only).                               | No       | `'never'`       |
| `validateAction`     | `string`                                                 | Name of a Redux action for server-side validation on blur.                       | No       |                 |
| `findReplace`        | `{ find: string, replace: string }`                      | Configuration for automatically replacing parts of the input value (e.g., slugify). | No       |                 |
| `contextualDescription`| `string`                                                 | Additional description text, often used with `findReplace`.                      | No       |                 |
| `hasQRScanner`       | `boolean`                                                | If true, displays a QR code scanner icon/button.                                 | No       | `false`         |
| `qrScannerParamName` | `string`                                                 | The query parameter name to extract from the scanned QR code URL.                | No       | `'invite_code'` |
| `hasCopy`            | `boolean`                                                | If true, displays a copy-to-clipboard icon/button.                               | No       | `false`         |
| `backgroundColor`    | `string`                                                 | Background color for the input container.                                        | No       |                 |
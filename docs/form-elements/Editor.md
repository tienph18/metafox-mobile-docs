# Editor

The same with element Text.

## Props

| Name                  | Type                                                              | Description                                                                 | Required | Default         |
| :-------------------- | :---------------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :-------------- |
| `label`        | `string`                                                          | The label displayed above the input field.                                  | No       |                 |
| `placeholder`  | `string`                                                          | Placeholder text shown when the input is empty.                             | No       |                 |
| `description`  | `string`                                                          | Help text displayed below the input field.                                  | No       |                 |
| `variant`      | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined' \| 'livestream'` | The visual style variant of the input field.                              | No       | `'standard'`    |
| `fullWidth`    | `boolean`                                                         | If `true`, the input field takes the full width of its container.           | No       | `false`         |
| `margin`       | `'none' \| 'normal' \| 'dense'`                                     | The margin applied around the form control.                                 | No       | `'normal'`      |
| `multiline`    | `boolean`                                                         | If `true`, allows multiple lines of text input (textarea).                  | No       | `false`         |
| `minHeight`    | `number`                                                          | Minimum height for the input field, especially useful with `multiline`.     | No       |                 |
| `maxLength`    | `number`                                                          | Maximum number of characters allowed in the input.                          | No       |                 |
| `autoFocus`    | `boolean`                                                         | If `true`, the input field automatically gains focus when mounted.          | No       | `false`         |
| `autoCorrect`  | `boolean`                                                         | Enables or disables auto-correction for the input.                          | No       | `true`          |
| `autoCapitalize`| `'none' \| 'sentences' \| 'words' \| 'characters'`                | Controls automatic capitalization behavior.                                 | No       | `'sentences'`   |
| `editable`     | `boolean`                                                         | If `false`, the text input is not editable.                                 | No       | `true`          |
| `required`     | `boolean`                                                         | Visually marks the field as required (e.g., with an asterisk).              | No       | `false`         |
| `clearButtonMode`| `'never' \| 'while-editing' \| 'unless-editing' \| 'always'`      | (iOS only) When to display the clear text button.                           | No       | `'never'`       |
| `validateAction`| `string`                                                          | Name of a registered action for backend validation triggered on blur.       | No       |                 |
| `findReplace`  | `{ find: string, replace: string }`                               | Configuration to automatically generate a slug-like value based on input. | No       |                 |
| `contextualDescription` | `string`                                               | Additional descriptive text displayed near the input.                       | No       |                 |
| `hasQRScanner` | `boolean`                                                         | If `true`, displays a QR code scanner icon button.                          | No       | `false`         |
| `qrScannerParamName` | `string`                                                  | Query parameter name to extract from the scanned QR code URL.               | No       | `'invite_code'` |
| `hasCopy`      | `boolean`                                                         | If `true`, displays a copy-to-clipboard icon button.                        | No       | `false`         |
| `backgroundColor`| `string`                                                          | Sets the background color for the input wrapper.                            | No       |                 |
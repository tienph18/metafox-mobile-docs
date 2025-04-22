# SFText

The `SFText` element renders a standard text input field within a form. It supports various configurations like multiline input, validation, QR code scanning, and copy-to-clipboard functionality.

## Props

| Name                 | Type                                                     | Description                                                                 | Required | Default         |
| -------------------- | -------------------------------------------------------- | --------------------------------------------------------------------------- | -------- | --------------- |
| `label`              | `string`                                                 | The label displayed above the input.                                        | No       | `undefined`     |
| `placeholder`        | `string`                                                 | Placeholder text shown when the input is empty.                             | No       | `undefined`     |
| `description`        | `string`                                                 | Help text displayed below the input.                                        | No       | `undefined`     |
| `contextualDescription` | `string`                                              | Additional description text.                                                | No       | `undefined`     |
| `variant`            | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'`, `'livestream'` | Visual style of the input.                                                  | No       | `'standard'`    |
| `fullWidth`          | `boolean`                                                | Makes the input take the full width.                                        | No       | `false`         |
| `margin`             | `'none'`, `'dense'`, `'normal'`                          | Controls the margin around the element.                                     | No       | `'normal'`      |
| `paddingBottom`      | `'none'`, `'dense'`, `'normal'`                          | Controls the bottom padding.                                                | No       | `'normal'`      |
| `required`           | `boolean`                                                | Marks the field as required (visual indicator).                             | No       | `false`         |
| `disabled`           | `boolean`                                                | Disables the input field (passed directly, not in `config`).                | No       | `false`         |
| `editable`           | `boolean`                                                | If `false`, the text is not editable.                                       | No       | `true`          |
| `multiline`          | `boolean`                                                | Allows multiple lines of text input.                                        | No       | `false`         |
| `minHeight`          | `number`                                                 | Minimum height for the input, useful for multiline.                         | No       | `undefined`     |
| `maxLength`          | `number`                                                 | Maximum number of characters allowed.                                       | No       | `undefined`     |
| `autoCorrect`        | `boolean`                                                | Enables auto-correction.                                                    | No       | `true`          |
| `autoCapitalize`     | `'none'`, `'sentences'`, `'words'`, `'characters'`       | Controls automatic capitalization.                                          | No       | `'sentences'`   |
| `autoFocus`          | `boolean`                                                | Automatically focuses the input on mount.                                   | No       | `false`         |
| `clearButtonMode`    | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls the visibility of the clear button (iOS only).                     | No       | `'never'`       |
| `validateAction`     | `string`                                                 | Action name for backend validation on blur.                                 | No       | `undefined`     |
| `findReplace`        | `{ find: string, replace: string }`                      | Defines find/replace rules for generating a slug displayed below the input. | No       | `undefined`     |
| `hasQRScanner`       | `boolean`                                                | Adds a QR code scanner icon/button.                                         | No       | `false`         |
| `qrScannerParamName` | `string`                                                 | Query parameter name to extract from the scanned QR code URL.               | No       | `'invite_code'` |
| `hasCopy`            | `boolean`                                                | Adds a copy-to-clipboard icon/button.                                       | No       | `false`         |
| `backgroundColor`    | `string`                                                 | Sets the background color of the input.                                     | No       | `undefined`     |
| `order`              | `number`                                                 | Order of the element in the form.                                           | No       | `undefined`     |
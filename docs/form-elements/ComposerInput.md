# ComposerInput

A specialized text input field designed for composer interfaces within MetaFox forms. It renders an input area that, when pressed, opens a bottom sheet for text entry. It supports dynamic height adjustment based on content.

## Props

| Name                  | Type                                                      | Description                                                                 | Required | Default     |
| :-------------------- | :-------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :---------- |
| `label`               | `string`                                                  | The text label displayed for the input.                                     | No       | `undefined` |
| `placeholder`         | `string`                                                  | Placeholder text shown when the input is empty.                             | No       | `undefined` |
| `description`         | `string`                                                  | Help text displayed below the input.                                        | No       | `undefined` |
| `variant`             | `'standard' \| 'outlined' \| 'filled'`                    | The visual style variant of the input.                                      | No       | `'standard'`|
| `margin`              | `'none' \| 'dense' \| 'normal'`                           | Controls the margin around the component.                                   | No       | `'normal'`  |
| `fullWidth`           | `boolean`                                                 | If `true`, the component takes up the full width of its container.          | No       | `false`     |
| `required`            | `boolean`                                                 | Visually marks the field as required (e.g., with an asterisk).              | No       | `false`     |
| `disabled`            | `boolean`                                                 | If `true`, the input field is disabled.                                     | No       | `false`     |
| `maxLength`           | `number`                                                  | Maximum number of characters allowed in the input.                          | No       | `undefined` |
| `autoFocus`           | `boolean`                                                 | If `true`, the input field automatically gains focus when mounted.          | No       | `false`     |
| `autoCorrect`         | `boolean`                                                 | Enables or disables auto-correction.                                        | No       | `undefined` |
| `autoCapitalize`      | `'none' \| 'sentences' \| 'words' \| 'characters'`        | Controls automatic capitalization behavior.                                 | No       | `undefined` |
| `clearButtonMode`     | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | (iOS only) When to display the standard clear button.                       | No       | `undefined` |
| `findReplace`         | `{ find: string, replace: string }`                       | Defines patterns for automatic find-and-replace operations on the value.    | No       | `undefined` |
| `contextualDescription`| `string`                                                  | Additional description text, often appended with the current field value. | No       | `undefined` |
# Textarea

Provides a multi-line text input field for forms.

## Props

| Name                  | Type                                               | Description                                                                                                | Required | Default          |
| :-------------------- | :------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :--------------- |
| `name`                | `string`                                           | The name of the field used in the form state.                                                              | Yes      |                  |
| `label`               | `string`                                           | The label displayed for the field.                                                                         | No       |                  |
| `placeholder`         | `string`                                           | Placeholder text shown when the input is empty.                                                            | No       |                  |
| `description`         | `string`                                           | Helper text displayed below the input field.                                                               | No       |                  |
| `required`            | `boolean`                                          | Marks the field as required, often visually indicated.                                                     | No       | `false`          |
| `disabled`            | `boolean`                                          | If true, the input field is disabled and cannot be interacted with.                                        | No       | `false`          |
| `fullWidth`           | `boolean`                                          | If true, the component stretches to the full width of its container.                                       | No       | `false`          |
| `margin`              | `'none' \| 'normal' \| 'dense'`                    | Controls the margin spacing around the field.                                                              | No       | `'normal'`       |
| `variant`             | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | The visual style variant of the input field.                                                               | No       | `'standard'`     |
| `minHeight`           | `number`                                           | Specifies the minimum height of the textarea input area in pixels.                                         | No       |                  |
| `maxLength`           | `number`                                           | Maximum number of characters allowed in the input.                                                         | No       |                  |
| `autoFocus`           | `boolean`                                          | If true, the input field automatically gains focus when the component mounts.                              | No       | `false`          |
| `autoCorrect`         | `boolean`                                          | Enables or disables autocorrection for the input.                                                          | No       | Platform default |
| `autoCapitalize`      | `'none' \| 'sentences' \| 'words' \| 'characters'` | Controls the automatic capitalization behavior of the text input.                                          | No       | `'none'`         |
| `editable`            | `boolean`                                          | If false, the text content cannot be modified by the user.                                                 | No       | `true`           |
| `clearButtonMode`     | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | (iOS only) Determines when the standard clear text button appears inside the text input.                 | No       | `'never'`        |
| `findReplace`         | `{ find: string, replace: string }`                | Defines patterns for find-and-replace operations on the input value, often used for generating derived text. | No       |                  |
| `contextualDescription`| `string`                                           | Additional description text that might be combined with dynamic content based on the input value.          | No       |                  |
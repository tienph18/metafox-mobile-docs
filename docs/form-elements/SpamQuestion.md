# SpamQuestion

This element renders a text input field, often accompanied by an image, designed to present a question to the user to prevent spam submissions. It integrates with Formik for state management.

## Props

| Name                 | Type                                                              | Description                                                                 | Required | Default            |
| :------------------- | :---------------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------------- |
| `label`              | `string`                                                          | The text label displayed for the field.                                     | No       |                    |
| `placeholder`        | `string`                                                          | Placeholder text shown in the input field when empty.                       | No       |                    |
| `required`           | `boolean`                                                         | Indicates if the field must be filled out.                                  | No       | `false`            |
| `disabled`           | `boolean`                                                         | Disables the input field, making it non-interactive.                        | No       | `false`            |
| `fullWidth`          | `boolean`                                                         | If `true`, the component will expand to take up the full available width.   | No       | `false`            |
| `margin`             | `'none' \| 'dense' \| 'normal'`                                   | Controls the margin spacing around the component.                           | No       | `undefined`        |
| `variant`            | `'standard' \| 'outlined' \| 'filled' \| 'standard-inlined'`      | Defines the visual style of the input field.                                | No       | `'standard-inlined'` |
| `imageUri`           | `string`                                                          | The URI for the image associated with the spam question.                    | Yes      |                    |
| `editable`           | `boolean`                                                         | Determines if the text input field can be edited by the user.               | No       | `true`             |
| `clearButtonMode`    | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | Controls when the clear text button appears in the input field (iOS only). | No       | `undefined`        |
| `paddingBottom`      | `'none' \| 'dense' \| 'normal'`                                   | Controls the padding at the bottom of the component.                        | No       | `undefined`        |
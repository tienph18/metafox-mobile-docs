# MembershipQuestion

The `MembershipQuestion` form element allows users to define a question with different answer formats (Checkbox, Multiple Choice, or Written Answer) typically used for group membership applications. It includes fields for the question text, selecting the answer type, and managing answer options if applicable.

## Props

| Name                 | Type                                                       | Description                                                                      | Required | Default     |
| :------------------- | :--------------------------------------------------------- | :------------------------------------------------------------------------------- | :------- | :---------- |
| `label`              | string                                                     | The label text displayed above the element.                                      | No       | `undefined` |
| `description`        | string                                                     | Additional descriptive text displayed below the label.                           | No       | `undefined` |
| `required`           | boolean                                                    | Marks the field as required (visually).                                          | No       | `false`     |
| `multiline`          | boolean                                                    | Allows the question input field to accept multiple lines.                        | No       | `false`     |
| `clearButtonMode`    | 'never' \| 'while-editing' \| 'unless-editing' \| 'always' | Determines when the clear button appears on the text input (iOS only).           | No       | `undefined` |
| `disabled`           | boolean                                                    | Disables the entire form element.                                                | No       | `false`     |
| `maxLength`          | number                                                     | Maximum number of answer options allowed for Checkbox/Multiple Choice types.     | No       | `5`         |
| `editable`           | boolean                                                    | Determines if the question text input can be edited.                             | No       | `true`      |
| `minHeight`          | number                                                     | Sets the minimum height for the question text input.                             | No       | `undefined` |
| `paddingBottom`      | string \| number                                           | Adds padding to the bottom of the form control.                                  | No       | `undefined` |
| `margin`             | string                                                     | Sets the margin around the form control.                                         | No       | `undefined` |
| `fullWidth`          | boolean                                                    | Makes the form control occupy the full available width.                          | No       | `false`     |
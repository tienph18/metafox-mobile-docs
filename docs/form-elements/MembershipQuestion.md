# MembershipQuestion

The `MembershipQuestion` form element allows users to define a question with different answer formats (Checkbox, Multiple Choice, or Written Answer) typically used for group membership applications. It includes fields for the question text, selecting the answer type, and managing answer options if applicable.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `label` | `string` | The label text displayed above the element. | | `undefined` |
| `description` | `string` | Additional descriptive text displayed below the label. | | `undefined` |
| `required` | `boolean` | Marks the field as required (visually). | | `false` |
| `multiline` | `boolean` | Allows the question input field to accept multiple lines. | | `false` |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Determines when the clear button appears on the text input (iOS only). | | `undefined` |
| `disabled` | `boolean` | Disables the entire form element. | | `false` |
| `maxLength` | `number` | Maximum number of answer options allowed for Checkbox/Multiple Choice types. | | `5` |
| `editable` | `boolean` | Determines if the question text input can be edited. | | `true` |
| `minHeight` | `number` | Sets the minimum height for the question text input. | | `undefined` |
| `paddingBottom` | `string`, `number` | Adds padding to the bottom of the form control. | | `undefined` |
| `margin` | `string` | Sets the margin around the form control. | | `undefined` |
| `fullWidth` | `boolean` | Makes the form control occupy the full available width. | | `false` |
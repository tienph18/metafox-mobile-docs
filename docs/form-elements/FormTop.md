# FormTop

Renders a top section for a form, optionally displaying a label and description, and rendering a collection of nested form elements.

## Props

| Name        | Type                          | Description                                                              | Required | Default     |
| :---------- | :---------------------------- | :----------------------------------------------------------------------- | :------- | :---------- |
| `label`     | `string`                      | Optional label text displayed at the top.                                | No       | `undefined` |
| `description`| `string`                      | Optional description text displayed below the label.                     | No       | `undefined` |
| `elements`  | `Record<string, FormFieldConfig>` | Object containing configurations for nested form elements to be rendered. | Yes      | N/A         |
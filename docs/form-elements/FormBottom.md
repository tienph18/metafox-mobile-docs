# FormBottom

Renders a styled container at the bottom of a form, typically used to group related elements like submit buttons or secondary actions. It can display an optional label and description, and renders a collection of nested form elements.

## Props

| Name        | Type                          | Description                                                                                             | Required | Default   |
| :---------- | :---------------------------- | :------------------------------------------------------------------------------------------------------ | :------- | :-------- |
| `label`     | `string`                      | Optional label text displayed above the elements.                                                       | No       | `undefined` |
| `description`| `string`                      | Optional description text displayed below the label.                                                    | No       | `undefined` |
| `elements`  | `Record<string, FormFieldConfig>` | An object containing configurations for nested form elements to be rendered within this section. | Yes      | `{}`      |
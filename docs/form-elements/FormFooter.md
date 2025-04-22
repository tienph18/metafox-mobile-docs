# FormFooter

Renders a footer section for a form, capable of displaying a label, description, and nested form elements.

## Props

| Name        | Type                         | Description                                                              | Required | Default |
| :---------- | :--------------------------- | :----------------------------------------------------------------------- | :------- | :------ |
| `label`     | `string`                     | An optional label for the footer section.                                | No       | `null`  |
| `description` | `string`                     | An optional description for the footer section.                          | No       | `null`  |
| `elements`  | `Record<string, ElementConfig>` | An object containing configurations for nested form elements.          | Yes      | `{}`    |
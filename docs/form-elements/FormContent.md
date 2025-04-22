# FormContent

The `FormContent` element acts as a container to group and render other form elements defined in its configuration. It can optionally display a label and description above the nested elements.

## Props

| Name        | Type                          | Description                                               | Required | Default   |
| :---------- | :---------------------------- | :-------------------------------------------------------- | :------- | :-------- |
| `label`     | `string`                      | Optional label text displayed above the content area.     | No       | `undefined` |
| `description`| `string`                      | Optional description text displayed below the label.      | No       | `undefined` |
| `elements`  | `Record<string, ElementConfig>` | An object containing configurations for nested elements. | Yes      | N/A       |
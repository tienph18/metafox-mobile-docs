# Chip

Renders a group of selectable chip buttons. Selecting a chip updates the form's `title` and `description` fields with the corresponding values from the selected option.

## Props

| Name            | Type                  | Description                                                                                      | Required | Default     |
| :-------------- | :-------------------- | :----------------------------------------------------------------------------------------------- | :------- | :---------- |
| `label`         | `string`              | The text label displayed above the chips.                                                        | Yes      |             |
| `options`       | `RadioFieldOptions[]` | An array of option objects to render as chips. Each should have `title` and `description`.       | Yes      | `[]`        |
| `required`      | `boolean`             | Marks the field as required, adding a visual indicator to the label.                             | No       | `false`     |
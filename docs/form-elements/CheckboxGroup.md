# CheckboxGroup

This element renders a group of checkboxes, allowing users to select multiple options from a predefined list. It integrates with Formik for state management and validation.

## Props

| Name             | Type                                     | Description                                                                 | Required | Default      |
| :--------------- | :--------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `label`          | `string`                                 | The text label displayed above the checkbox group.                          | Yes      |              |
| `options`        | `Array<{ label: string, value: any }>` | An array of objects defining the available checkbox options.                | Yes      | `[]`         |
| `variant`        | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the form control wrapper.                       | No       | `'standard'` |
| `margin`         | `'normal' \| 'dense' \| 'none'`        | The margin applied around the form control.                                 | No       | `undefined`  |
| `fullWidth`      | `boolean`                                | If `true`, the form control spans the full width of its container.          | No       | `false`      |
| `disabled`       | `boolean`                                | If `true`, all checkboxes in the group are disabled.                        | No       | `false`      |
| `required`       | `boolean`                                | If `true`, the field is marked as required in the UI.                       | No       | `false`      |
| `hasFormOrder`   | `boolean`                                | If `true`, prepends the `order` number to the label.                        | No       | `false`      |
| `order`          | `number`                                 | The numerical order to display before the label (if `hasFormOrder` is true). | No       | `undefined`  |
| `paddingBottom`  | `string`                                 | Custom padding applied to the bottom of the form control.                   | No       | `undefined`  |
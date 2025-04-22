# RadioLabelGroup

Renders a group of radio buttons, visually styled using circular icons, allowing the user to select only one option from a list. This element is typically used for membership questions or similar single-choice scenarios within a form.

## Props

| Name              | Type                                                                 | Description                                                                                                | Required | Default     |
| :---------------- | :------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :---------- |
| `label`           | `string`                                                             | The main label displayed above the radio group.                                                            | Yes      |             |
| `options`         | `Array<{ value: string, label?: string, disable?: boolean }>`        | An array of objects defining each radio option. `value` is required, `label` and `disable` are optional. | Yes      | `[]`        |
| `variant`         | `'standard' \| 'outlined' \| 'filled' \| string`                     | The visual style variant of the form control.                                                              | No       | `'standard'`|
| `margin`          | `'normal' \| 'dense' \| 'none' \| string`                            | Defines the margin spacing for the form control.                                                           | No       | `'normal'`  |
| `fullWidth`       | `boolean`                                                            | If `true`, the form control will occupy the full width of its container.                                   | No       | `false`     |
| `disabled`        | `boolean`                                                            | If `true`, the entire radio group will be disabled. Can also be set via the top-level `disabled` prop.   | No       | `false`     |
| `required`        | `boolean`                                                            | If `true`, marks the field as required (e.g., adds an asterisk to the label).                              | No       | `false`     |
| `hasFormOrder`    | `boolean`                                                            | If `true`, prepends the `order` number to the `label`.                                                     | No       | `false`     |
| `order`           | `number`                                                             | The numerical order to display before the label when `hasFormOrder` is `true`.                             | No       |             |
| `paddingBottom`   | `string`                                                             | Adds padding to the bottom of the form control.                                                            | No       |             |
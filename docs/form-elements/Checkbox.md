# Checkbox

A form element that renders a checkbox input field. It allows users to toggle between a checked and unchecked state, typically representing a boolean value or a specific selection.

## Props

| Name                | Type                                                   | Description                                                     | Required | Default            |
| :------------------ | :----------------------------------------------------- | :-------------------------------------------------------------- | :------- | :----------------- |
| `label`             | `string`                                               | The text label displayed next to the checkbox.                  | Yes      |                    |
| `fullWidth`         | `boolean`                                              | If true, the control takes up the full available width.         | No       | `false`            |
| `margin`            | `'none' \| 'dense' \| 'normal'`                        | Margin size around the control.                                 | No       | `'normal'`         |
| `required`          | `boolean`                                              | Whether the field is required (validation).                     | No       | `false`            |
| `variant`           | `'standard' \| 'outlined' \| 'filled' \| 'standard-inlined'` | Visual style variant of the control.                            | No       | `'standard-inlined'` |
| `paddingBottom`     | `'none' \| 'dense' \| 'normal'`                        | Padding below the control.                                      | No       | `'normal'`         |
| `checkedValue`      | `any`                                                  | The value submitted when the checkbox is checked.               | No       | `1`                |
| `uncheckedValue`    | `any`                                                  | The value submitted when the checkbox is unchecked.             | No       | `0`                |
| `description`       | `string`                                               | Additional descriptive text displayed below the label.          | No       | `''`               |
| `disabled`          | `boolean`                                              | If true, the checkbox is disabled and cannot be interacted with. | No       | `false`            |
| `isReverse`         | `boolean`                                              | If true, reverses the order of the label and checkbox control.  | No       | `false`            |
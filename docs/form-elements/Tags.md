# Tags

A form element that allows users to input and manage a list of tags. Users can type tags and press Enter/Done to add them. Existing tags can be removed by clicking the close icon on the tag.

## Props

| Name             | Type                                                     | Description                                                                 | Required | Default      |
| :--------------- | :------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `label`          | `string`                                                 | The text label displayed for the field.                                     | No       |              |
| `description`    | `string`                                                 | Helper text displayed below the input.                                      | No       |              |
| `placeholder`    | `string`                                                 | Placeholder text shown when the input is empty.                             | No       | `'enter text'` |
| `variant`        | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | The visual style variant of the input.                                      | No       | `'standard'` |
| `fullWidth`      | `boolean`                                                | If true, the element spans the full width of its container.                 | No       | `false`      |
| `margin`         | `'normal' \| 'dense' \| 'none'`                          | Controls the margin around the form control.                                | No       |              |
| `required`       | `boolean`                                                | Marks the field as mandatory.                                               | No       | `false`      |
| `paddingBottom`  | `'normal' \| 'dense' \| 'none'`                          | Controls the bottom padding of the form control.                            | No       | `'normal'`   |
| `clearButtonMode`| `string`                                                 | Determines the visibility of the clear button (standard TextInput prop).    | No       |              |
| `editable`       | `boolean`                                                | If false, the input cannot be edited (standard TextInput prop).             | No       | `true`       |
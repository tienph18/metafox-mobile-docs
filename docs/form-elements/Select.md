# Select

The `Select` form element provides a dropdown or list interface for users to choose one or multiple options from a predefined set. It supports various configurations like search, multiple selections, and different visual styles.

## Props

| Name                 | Type                                                                                             | Description                                                                 | Required | Default     |
| :------------------- | :----------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :---------- |
| `label`              | `string`                                                                                         | The text label displayed for the select field.                              | Yes      |             |
| `options`            | `OptionsItemShape[]`                                                                             | An array of available options for the select field.                         | Yes      | `[]`        |
| `fullWidth`          | `boolean`                                                                                        | If `true`, the select field takes up the full width of its container.       | No       | `false`     |
| `margin`             | `'none' \| 'dense' \| 'normal'`                                                                  | Defines the margin spacing around the select field.                         | No       | `'normal'`  |
| `required`           | `boolean`                                                                                        | If `true`, the field must have a value.                                     | No       | `false`     |
| `variant`            | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined' \| 'livestream'`                    | The visual style variant of the select field.                               | No       | `'standard'`|
| `paddingBottom`      | `'none' \| 'dense' \| 'normal'`                                                                  | Defines the bottom padding spacing for the select field.                    | No       | `'normal'`  |
| `suboptions`         | `SubOptionsShape`                                                                                | Additional options grouped under main options (e.g., for dependent selects). | No       | `undefined` |
| `multiple`           | `boolean`                                                                                        | If `true`, allows selecting multiple options.                               | No       | `false`     |
| `disable_custom`     | `boolean`                                                                                        | If `true`, disables the ability to add custom options (if applicable).      | No       | `false`     |
| `value_type`         | `string`                                                                                         | Specifies the type of value to store (e.g., 'array').                       | No       | `undefined` |
| `enable_search`      | `boolean`                                                                                        | If `true`, enables a search input within the options list.                  | No       | `false`     |
| `disableClearable`   | `boolean`                                                                                        | If `true`, prevents the user from clearing the selected value.              | No       | `false`     |
| `choice_type`        | `string`                                                                                         | Specifies the type of choice control (e.g., 'radio', 'checkbox').           | No       | `undefined` |
| `placeholder`        | `string`                                                                                         | Placeholder text displayed when no value is selected.                       | No       | `'select'`  |
| `showWithoutOptions` | `boolean`                                                                                        | If `true`, renders the field even if the `options` array is empty.          | No       | `false`     |
| `useSectionList`     | `boolean`                                                                                        | If `true`, uses a SectionList to display options (requires specific data structure). | No       | `false`     |
| `disabled`           | `boolean`                                                                                        | If `true`, the select field is disabled and cannot be interacted with.      | No       | `false`     |
| `description`        | `string`                                                                                         | Additional text displayed below the select field for guidance.              | No       | `undefined` |
| `resetValue`         | `boolean`                                                                                        | If `true`, indicates the value should be reset under certain conditions.    | No       | `false`     |
# SFSelect

The `SFSelect` element provides a dropdown-like selection interface, typically opening a bottom sheet for users to choose one or multiple options from a list. It supports features like search, sections, and conditional options based on other fields.

## Props

| Name                 | Type                               | Description                                                                 | Required | Default     |
| :------------------- | :--------------------------------- | :-------------------------------------------------------------------------- | :------- | :---------- |
| `label`              | `string`                           | The label displayed for the form element.                                   | Yes      | `undefined` |
| `options`            | `OptionsItemShape[]`               | The list of selectable options.                                             | Yes      | `[]`        |
| `fullWidth`          | `boolean`                          | If true, the component takes up the full width.                             | No       | `false`     |
| `margin`             | `'dense' \| 'normal' \| 'none'`    | Margin size.                                                                | No       | `'normal'`  |
| `required`           | `boolean`                          | Whether the field is required.                                              | No       | `false`     |
| `variant`            | `'standard' \| 'outlined' \| etc.` | Visual style variant.                                                       | No       | `'standard'`|
| `paddingBottom`      | `'dense' \| 'normal' \| 'none'`    | Bottom padding size.                                                        | No       | `'normal'`  |
| `suboptions`         | `SubOptionsShape`                  | Additional options grouped under main options.                              | No       | `undefined` |
| `initialValue`       | `OptionsItemShape[]`               | Initial selected value(s).                                                  | No       | `undefined` |
| `disable_custom`     | `boolean`                          | Disables custom privacy options if applicable.                              | No       | `false`     |
| `value_type`         | `string`                           | Specifies the type of value expected (e.g., 'string', 'number').            | No       | `undefined` |
| `multiple`           | `boolean`                          | Allows multiple selections if true.                                         | No       | `false`     |
| `enable_search`      | `boolean`                          | Enables searching within the options list in the bottom sheet.              | No       | `false`     |
| `disableClearable`   | `boolean`                          | Prevents clearing/unselecting the chosen option(s).                         | No       | `false`     |
| `choice_type`        | `string`                           | Type of choice mechanism (used internally, e.g., 'radio', 'checkbox').      | No       | `undefined` |
| `placeholder`        | `string`                           | Placeholder text displayed when no value is selected.                       | No       | `undefined` |
| `showWithoutOptions` | `boolean`                          | Renders the component even if no `options` are provided.                    | No       | `false`     |
| `useSectionList`     | `boolean`                          | Uses a SectionList for displaying options in the bottom sheet if true.      | No       | `false`     |
| `autoSubmit`         | `boolean`                          | Submits the form automatically on value change.                             | No       | `false`     |
| `relatedFieldName`   | `string`                           | Name of a related form field for conditional logic (e.g., filtering options). | No       | `undefined` |
| `optionRelatedMapping`| `Record<string, OptionsItemShape[]>`| Mapping object for options based on the `relatedFieldName`'s value.         | No       | `undefined` |
| `resetValue`         | `boolean`                          | Resets the value under certain conditions (used internally).                | No       | `false`     |
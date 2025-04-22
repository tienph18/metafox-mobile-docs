# FriendPicker

A form element that allows users to select one or multiple friends from a list, typically fetched via an API. It presents a user-friendly interface for friend selection within forms.

## Props

| Name              | Type                                                                              | Description                                       | Required | Default     |
| :---------------- | :-------------------------------------------------------------------------------- | :------------------------------------------------ | :------- | :---------- |
| `fullWidth`       | `boolean`                                                                         | Controls if the element takes the full width.     | No       | `false`     |
| `margin`          | `'none' \| 'dense' \| 'normal'`                                                   | Sets the margin around the element.               | No       | `'normal'`  |
| `required`        | `boolean`                                                                         | Marks the field as required.                      | No       | `false`     |
| `variant`         | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined' \| 'livestream'` | Sets the visual style of the element.             | No       | `'standard'`|
| `paddingBottom`   | `'none' \| 'dense' \| 'normal'`                                                   | Sets the bottom padding.                          | No       | `undefined` |
| `label`           | `string`                                                                          | The label displayed for the field.                | No       | `''`        |
| `suboptions`      | `SubOptionsShape`                                                                 | Additional options or configurations.             | No       | `undefined` |
| `initialValue`    | `OptionsItemShape[]`                                                              | Initial selected friend(s).                       | No       | `undefined` |
| `disable_custom`  | `boolean`                                                                         | Disables custom privacy selection.                | No       | `false`     |
| `value_type`      | `string`                                                                          | Specifies the type of value returned.             | No       | `undefined` |
| `multiple`        | `boolean`                                                                         | Allows selecting multiple friends.                | No       | `false`     |
| `options`         | `OptionsItemShape[]`                                                              | Predefined list of options.                       | No       | `[]`        |
| `enable_search`   | `boolean`                                                                         | Enables searching within the friend list.         | No       | `false`     |
| `disable_uncheck` | `boolean`                                                                         | Prevents unselecting if required.                 | No       | `false`     |
| `choice_type`     | `string`                                                                          | Type of choice mechanism.                         | No       | `undefined` |
| `placeholder`     | `string`                                                                          | Placeholder text when no value is selected.       | No       | `undefined` |
| `showWithoutOptions`| `boolean`                                                                         | Whether to show the field without options.        | No       | `undefined` |
| `api_endpoint`    | `string`                                                                          | API endpoint to fetch friend suggestions.         | Yes      | `undefined` |
| `disabled`        | `boolean`                                                                         | Disables the field input.                         | No       | `false`     |
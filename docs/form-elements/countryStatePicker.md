# countryStatePicker

This element provides a specialized picker for selecting a country and its corresponding state or province. It typically fetches state/province options dynamically based on the selected country.

## Props

| Name              | Type                                  | Description                                                                 | Required | Default     |
| :---------------- | :------------------------------------ | :-------------------------------------------------------------------------- | :------- | :---------- |
| `label`           | `string`                              | The text label displayed for the element.                                   | Yes      | `''`        |
| `fullWidth`       | `boolean`                             | If true, the element takes the full width.                                  | No       | `false`     |
| `margin`          | `'normal' \| 'dense' \| 'none'`       | Controls the margin around the element.                                     | No       | `'normal'`  |
| `required`        | `boolean`                             | If true, the field is mandatory.                                            | No       | `false`     |
| `variant`         | `'standard' \| 'outlined' \| 'filled'`| The display style of the form element.                                      | No       | `'standard'`|
| `paddingBottom`   | `'normal' \| 'dense' \| 'none'`       | Controls the bottom padding.                                                | No       | `'normal'`  |
| `placeholder`     | `string`                              | Placeholder text when no value is selected.                                 | No       | `undefined` |
| `search_endpoint` | `string`                              | API endpoint to fetch options dynamically (e.g., states based on country). | No       | `undefined` |
| `search_params`   | `object`                              | Additional parameters for the search API endpoint.                          | No       | `undefined` |
| `enable_search`   | `boolean`                             | Enables searching within the options list (if applicable).                  | No       | `false`     |
| `disable_uncheck` | `boolean`                             | Prevents unselecting the current value if the field is required.            | No       | `false`     |
| `backgroundColor` | `string`                              | Background color for the element (used in specific variants).               | No       | `undefined` |
| `disabled`        | `boolean`                             | If true, the element is disabled.                                           | No       | `false`     |
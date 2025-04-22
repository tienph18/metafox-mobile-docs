# CountryCityCode

This form element provides an input field that allows users to select a country and associated city/state code. It typically opens a dedicated selection interface (modal or screen) for browsing and choosing the appropriate code.

## Props

| Name              | Type                                             | Description                                                                                              | Required | Default        |
| :---------------- | :----------------------------------------------- | :------------------------------------------------------------------------------------------------------- | :------- | :------------- |
| `label`           | `string`                                         | The label displayed for the form field and used as the title in the selection view.                      | Yes      | `''`           |
| `fullWidth`       | `boolean`                                        | If true, the component takes up the full width of its container.                                         | No       | `false`        |
| `margin`          | `'none' \| 'dense' \| 'normal'`                  | Defines the margin spacing around the component.                                                         | No       | `'normal'`     |
| `required`        | `boolean`                                        | Marks the field as required, often displaying an asterisk and preventing unselection.                    | No       | `false`        |
| `variant`         | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | The visual style variant of the form field.                                                              | No       | `'standard'`   |
| `paddingBottom`   | `'none' \| 'dense' \| 'normal'`                  | Defines the bottom padding spacing.                                                                      | No       | `'normal'`     |
| `enable_search`   | `boolean`                                        | Enables search functionality within the selection view.                                                  | No       | `false`        |
| `disable_uncheck` | `boolean`                                        | Prevents the user from unselecting the current value if set to true.                                     | No       | `false`        |
| `search_endpoint` | `string`                                         | API endpoint used for searching options if `enable_search` is true.                                      | No       | `undefined`    |
| `search_params`   | `object`                                         | Additional parameters for the search request. Values can be dynamically sourced from the form context. | No       | `undefined`    |
| `backgroundColor` | `string`                                         | Background color for the animated placeholder (used in 'standard-outlined' variant).                     | No       | `undefined`    |
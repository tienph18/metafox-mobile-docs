# Autocomplete

A form element allowing users to select one or multiple options from a list, often populated dynamically via an API search. It presents the selected value(s) and opens a dedicated interface for searching and selecting options.

## Props

| Name              | Type                                  | Description                                                                 | Required | Default      |
| :---------------- | :------------------------------------ | :-------------------------------------------------------------------------- | :------- | :----------- |
| `variant`         | `string` ('outlined', 'standard', ...) | Visual style of the form field.                                             | No       | `'outlined'` |
| `label`           | `string`                              | The text label displayed for the form field.                                | Yes      |              |
| `size`            | `string` ('medium', 'small')          | The size of the form field.                                                 | No       | `'medium'`   |
| `margin`          | `string` ('normal', 'dense', 'none')  | The margin applied around the form field.                                   | No       | `'normal'`   |
| `placeholder`     | `string`                              | Placeholder text displayed when no value is selected.                       | No       | `''`         |
| `required`        | `boolean`                             | Indicates if the field is mandatory (adds visual indicator).                | No       | `false`      |
| `fullWidth`       | `boolean`                             | If `true`, the form field occupies the full width of its container.         | No       | `true`       |
| `search_endpoint` | `string`                              | API endpoint URL used to fetch options dynamically based on user input.     | Yes      |              |
| `search_params`   | `object`                              | Additional parameters to include in the API request to `search_endpoint`.   | No       | `{}`         |
| `multiple`        | `boolean`                             | If `true`, allows the user to select multiple options.                      | No       | `false`      |
| `enable_search`   | `boolean`                             | If `true`, enables a search input within the selection interface.           | No       | `true`       |
| `disable_uncheck` | `boolean`                             | If `true`, prevents unselecting the currently selected option (single mode). | No       | `false`      |
| `choice_type`     | `string`                              | Influences how choices are presented or handled internally.                 | No       | `undefined`  |
| `icon`            | `string` (IconName)                   | Name of the icon to display, primarily used in the 'livestream' variant.    | No       | `undefined`  |
| `paddingBottom`   | `string` ('normal', 'dense', 'none')  | Specifies the bottom padding for the form control wrapper.                  | No       | `undefined`  |
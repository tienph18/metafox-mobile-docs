# SFAutocomplete

The `SFAutocomplete` element provides an autocomplete input field, allowing users to search and select one or multiple options from a predefined list or dynamically fetched data source. It opens a bottom sheet for option selection.

## Props

| Name              | Type                     | Description                                                                          | Required | Default    |
| :---------------- | :----------------------- | :----------------------------------------------------------------------------------- | :------- | :--------- |
| `fullWidth`       | `boolean`                | If true, the component takes up the full width.                                      | No       | `false`    |
| `margin`          | `normal`, `dense`, `none` | Margin size.                                                                         | No       | `normal`   |
| `required`        | `boolean`                | Whether the field is required.                                                       | No       | `false`    |
| `variant`         | `standard`, `outlined`   | Visual style variant.                                                                | No       | `standard` |
| `paddingBottom`   | `normal`, `dense`, `none` | Bottom padding size.                                                                 | No       | `normal`   |
| `label`           | `string`                 | The label text for the form element.                                                 | No       | `''`       |
| `multiple`        | `boolean`                | Allow multiple selections.                                                           | No       | `false`    |
| `disable_uncheck` | `boolean`                | Prevent unselecting the current value (makes selection required if a value exists). | No       | `false`    |
| `search_endpoint` | `string`                 | API endpoint URL to fetch options dynamically.                                       | No       | `undefined`|
| `search_params`   | `object`                 | Additional parameters for the search API endpoint.                                   | No       | `{}`       |
| `valueKey`        | `string`                 | Key to use for the option's value.                                                   | No       | `'id'`     |
| `labelKey`        | `string`                 | Key to use for the option's display label.                                           | No       | `'name'`   |
| `useOptionContext`| `boolean`                | Whether to use a shared option context for managing selected options.                | No       | `false`    |
| `option_default`  | `Array<any>`             | Default options to use if `useOptionContext` is true and no context value exists.    | No       | `[]`       |
| `canLoadMore`     | `boolean`                | Whether more options can be loaded (pagination) from the search endpoint.            | No       | `false`    |
| `placeholder`     | `string`                 | Placeholder text when no value is selected.                                          | No       | `undefined`|
| `options`         | `OptionsItemShape[]`     | Predefined options list (used if `search_endpoint` is not provided).                 | No       | `[]`       |
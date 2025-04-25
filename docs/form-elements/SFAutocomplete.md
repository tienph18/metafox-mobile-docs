## SFAutocomplete

The `SFAutocomplete` element provides an autocomplete input field, allowing users to search and select one or multiple options from a predefined list or dynamically fetched data source. It opens a bottom sheet for option selection.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `canLoadMore` | `boolean` | Whether more options can be loaded (pagination) from the search endpoint. | | `false` |
| `disable_uncheck` | `boolean` | Prevent unselecting the current value (makes selection required if a value exists). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | | `''` |
| `labelKey` | `string` | Key to use for the option's display label. | | `'name'` |
| `margin` | `normal`, `dense`, `none` | | | `normal` |
| `multiple` | `boolean` | Allow multiple selections. | | `false` |
| `option_default` | `Array<any>` | Default options to use if `useOptionContext` is true and no context value exists. | | `[]` |
| `options` | `OptionsItemShape[]` | Predefined options list (used if `search_endpoint` is not provided). | | `[]` |
| `paddingBottom` | `normal`, `dense`, `none` | | | `normal` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `search_endpoint` | `string` | API endpoint URL to fetch options dynamically. | | `undefined` |
| `search_params` | `object` | Additional parameters for the search API endpoint. | | `{}` |
| `useOptionContext` | `boolean` | Whether to use a shared option context for managing selected options. | | `false` |
| `valueKey` | `string` | Key to use for the option's value. | | `'id'` |
| `variant` | `standard`, `outlined` | Specifies the visual style of the component. | | `standard` |

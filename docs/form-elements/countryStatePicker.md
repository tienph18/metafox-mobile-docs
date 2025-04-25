## countryStatePicker

This element provides a specialized picker for selecting a country and its corresponding state or province. It typically fetches state/province options dynamically based on the selected country from `CountryCityCode`.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `backgroundColor` | `string` | Background color for the element (used in specific variants). | | `undefined` |
| `disable_uncheck` | `boolean` | Prevents unselecting the current value if the field is required. | | `false` |
| `disabled` | `boolean` | | | `false` |
| `enable_search` | `boolean` | Enables searching within the options list (if applicable). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | `''` |
| `margin` | `'normal' \| 'dense' \| 'none'` | | | `'normal'` |
| `paddingBottom` | `'normal' \| 'dense' \| 'none'` | | | `'normal'` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `search_endpoint` | `string` | API endpoint to fetch options dynamically (e.g., states based on country). | | `undefined` |
| `search_params` | `object` | Additional parameters for the search API endpoint. | | `undefined` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

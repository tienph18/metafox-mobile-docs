## SFFilterPrice

The `SFFilterPrice` element provides a form input for selecting a price range (minimum and maximum). It displays the selected range and opens a bottom sheet for users to enter or modify the 'from' and 'to' price values.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `enable_search` | `boolean` | Configuration passed to the bottom sheet component (FilterPriceField). | | `false` |
| `findReplace` | `any` | Configuration passed to the bottom sheet component (FilterPriceField). | | |
| `fromFieldLabel` | `string` | Label for the minimum price input in the bottom sheet. | | |
| `fromFieldName` | `string` | The formik field name for the minimum price value. | | `'price_from'` |
| `fromFieldPlaceholder` | `string` | Placeholder text for the minimum price input in the bottom sheet. | | |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `string` | | | |
| `paddingBottom` | `string` | | | |
| `required` | `boolean` | | | `false` |
| `toFieldLabel` | `string` | Label for the maximum price input in the bottom sheet. | | |
| `toFieldName` | `string` | The formik field name for the maximum price value. | | `'price_to'` |
| `toFieldPlaceholder` | `string` | Placeholder text for the maximum price input in the bottom sheet. | | |
| `variant` | `string` | Specifies the visual style of the component. | | `'standard'` |

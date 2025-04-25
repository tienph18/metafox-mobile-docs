## SFSearchBox

The `SFSearchBox` component renders a search input field integrated directly into the screen's header navigation bar. It automatically handles focus, clearing, and debounced value updates for form submission.

*Note: This element is only used in a search form.*

### Props

The component accepts standard `FormFieldProps` (`name`, `config`, `disabled`, `formik`). The primary configuration is done via the `config` object:

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none' \| 'sentences' \| 'words' \| 'characters'` | Auto-capitalization behavior. | | `'none'` |
| `autoCorrect` | `boolean` | Enable/disable auto-correction. | | `false` |
| `autoFocus` | `boolean` | | | `true` if empty |
| `clearButtonMode` | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | How the clear button behaves (iOS only). | | `undefined` |
| `description` | `string` | | | `undefined` |
| `editable` | `boolean` | If the input is editable. | | `true` |
| `fullWidth` | `boolean` | | | `false` |
| `margin` | `keyof typeof SizeEnum` | | | `undefined` |
| `maxLength` | `number` | | | `undefined` |
| `minHeight` | `number` | | | `undefined` |
| `multipleline` | `boolean` | If the input allows multiple lines. | | `false` |
| `paddingBottom` | `keyof typeof SizeEnum` | | | `undefined` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `showSearchIcon` | `boolean` | Whether to show the search icon. | | `true` |
| `variant` | `keyof typeof Variant` | Specifies the visual style of the component. | | `undefined` |

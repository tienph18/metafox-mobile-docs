## SFSelect

The `SFSelect` element provides a dropdown-like selection interface, typically opening a bottom sheet for users to choose one or multiple options from a list. It supports features like search, sections, and conditional options based on other fields.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoSubmit` | `boolean` | Submits the form automatically on value change. | | `false` |
| `choice_type` | `string` | Type of choice mechanism (used internally, e.g., 'radio', 'checkbox'). | | `undefined` |
| `disableClearable` | `boolean` | Prevents clearing/unselecting the chosen option(s). | | `false` |
| `disable_custom` | `boolean` | Disables custom privacy options if applicable. | | `false` |
| `enable_search` | `boolean` | Enables searching within the options list in the bottom sheet. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `OptionsItemShape[]` | Initial selected value(s). | | `undefined` |
| `label` | `string` | | Yes | `undefined` |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | `'normal'` |
| `multiple` | `boolean` | Allows multiple selections if true. | | `false` |
| `optionRelatedMapping` | `Record<string, OptionsItemShape[]>` | Mapping object for options based on the `relatedFieldName`'s value. | | `undefined` |
| `options` | `OptionsItemShape[]` | The list of selectable options. | Yes | `[]` |
| `paddingBottom` | `'dense' \| 'normal' \| 'none'` | | | `'normal'` |
| `placeholder` | `string` | | | `undefined` |
| `relatedFieldName` | `string` | Name of a related form field for conditional logic (e.g., filtering options). | | `undefined` |
| `required` | `boolean` | | | `false` |
| `resetValue` | `boolean` | Resets the value under certain conditions (used internally). | | `false` |
| `showWithoutOptions` | `boolean` | Renders the component even if no `options` are provided. | | `false` |
| `suboptions` | `SubOptionsShape` | Additional options grouped under main options. | | `undefined` |
| `useSectionList` | `boolean` | Uses a SectionList for displaying options in the bottom sheet if true. | | `false` |
| `value_type` | `string` | Specifies the type of value expected (e.g., 'string', 'number'). | | `undefined` |
| `variant` | `'standard' \| 'outlined' \| etc.` | Specifies the visual style of the component. | | `'standard'` |

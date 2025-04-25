## SFFilterForm

Renders a button that opens a bottom sheet containing a sub-form, typically used for applying filters within a larger form. Pressing the button navigates to a dedicated screen (`FORM_BOTTOM_SHEET`) where the filter options, defined by the `options` and `suboptions` props, are presented.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `choice_type` | `string` | Specifies the type of choice input used in the sub-form (e.g., 'checkbox'). | | `undefined` |
| `disable_custom` | `boolean` | Disables custom options in the sub-form. | | `false` |
| `disable_uncheck` | `boolean` | Prevents unselecting options once selected in the sub-form. | | `false` |
| `enable_search` | `boolean` | Enables a search input within the sub-form. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `OptionsItemShape[]` | Initial values for the filter options within the sub-form. | | `undefined` |
| `label` | `string` | | | `undefined` |
| `margin` | `normal` \| `dense` \| `none` | | | `normal` |
| `multiple` | `boolean` | Allows multiple selections in the sub-form. | | `false` |
| `options` | `OptionsItemShape[]` | The list of options to display within the sub-form. | Yes | `[]` |
| `paddingBottom` | `normal` \| `dense` \| `none` | | | `normal` |
| `placeholder` | `string` | | | `undefined` |
| `showWithoutOptions` | `boolean` | Determines if the filter button should be shown even when no options exist. | | `false` |
| `suboptions` | `SubOptionsShape` | Configuration for the sub-form displayed in the bottom sheet. | Yes | `undefined` |
| `useSectionList` | `boolean` | Uses a `SectionList` for displaying options in the sub-form if true. | | `false` |
| `value_type` | `string` | Specifies the expected data type of the selected value(s) in the sub-form. | | `undefined` |
| `variant` | `standard` \| `outlined` \| `filled` | Specifies the visual style of the component. | | `standard` |

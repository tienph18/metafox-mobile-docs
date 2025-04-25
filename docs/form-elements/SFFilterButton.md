## SFFilterButton

This form element renders a button, typically represented by an icon. When pressed, it opens a bottom sheet containing a sub-form (`ui.SubFormBuilder`) based on the main form's schema. This allows users to configure and apply filter criteria, which are then reflected in the main form's values upon submission of the sub-form.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `choice_type` | `string` | Defines the selection mechanism (e.g., 'radio', 'checkbox'). | | `undefined` |
| `disable_custom` | `boolean` | If `true`, disables custom value input in the filter form. | | `false` |
| `disable_uncheck` | `boolean` | If `true`, prevents users from unselecting an already selected option. | | `false` |
| `enable_search` | `boolean` | If `true`, enables a search input within the filter form options. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `OptionsItemShape[]` | Default selected values for the filter options. | | `undefined` |
| `label` | `string` | | | `''` |
| `margin` | `keyof typeof SizeEnum` | | | `undefined` |
| `multiple` | `boolean` | If `true`, allows multiple selections in the filter form. | | `false` |
| `options` | `OptionsItemShape[]` | The list of available options to display in the filter form. | | `[]` |
| `paddingBottom` | `keyof typeof SizeEnum` | | | `undefined` |
| `placeholder` | `string` | | | `''` |
| `required` | `boolean` | | | `false` |
| `showWithoutOptions` | `boolean` | If `true`, the button is shown even when there are no `config.options`. | | `false` |
| `suboptions` | `SubOptionsShape` | Configuration for sub-options within the filter form. | | `undefined` |
| `useSectionList` | `boolean` | If `true`, uses a `SectionList` component to render options in the filter form. | | `false` |
| `value_type` | `string` | Specifies the expected data type of the filter value. | | `undefined` |
| `variant` | `keyof typeof Variant` | Specifies the visual style of the component. | | `'standard'` |

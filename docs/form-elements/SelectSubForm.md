## SelectSubForm

This element renders a touchable area displaying an icon and the label of the currently selected option. Tapping it opens a bottom sheet containing a sub-form where the user can select one or multiple options from a predefined list (`options` and `suboptions`).

### Props

The component accepts standard `FormFieldProps` (`name`, `disabled`, `formik`) and a `config` object with the following properties:

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `choice_type` | `string` | Defines the selection mechanism in the sub-form (e.g., 'radio', 'checkbox'). | | `undefined` |
| `disable_custom` | `boolean` | If true, disables the ability to add custom options in the sub-form. | | `false` |
| `disable_uncheck` | `boolean` | If true, prevents users from deselecting an already selected option. | | `false` |
| `enable_search` | `boolean` | If true, enables a search input within the sub-form. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `icon` | `string` | The name of the Lineficon icon to display next to the selected value. | Yes | `''` |
| `initialValue` | `any` | The initial value of the form field. | | `undefined` |
| `label` | `string` | | | `''` |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | `'normal'` |
| `multiple` | `boolean` | If true, allows multiple options to be selected in the sub-form. | | `false` |
| `options` | `OptionsItemShape[]` | An array of primary options to be displayed in the sub-form. | Yes | `[]` |
| `paddingBottom` | `'dense' \| 'normal' \| 'none'` | | | `undefined` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `showWithoutOptions` | `boolean` | If true, the element is rendered even when no `options` are provided. | | `false` |
| `suboptions` | `SubOptionsShape` | An object containing secondary options, often dependent on the primary selection. | | `undefined` |
| `useSectionList` | `boolean` | If true, the sub-form uses a `SectionList` for displaying options, suitable for grouped data. | | `false` |
| `value_type` | `string` | Specifies the data type of the value (e.g., 'string', 'number'). | | `undefined` |
| `variant` | `'standard' \| 'outlined' \| ...` | Specifies the visual style of the component. | | `'standard'` |

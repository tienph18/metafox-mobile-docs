# SelectSubForm

This element renders a touchable area displaying an icon and the label of the currently selected option. Tapping it opens a bottom sheet containing a sub-form where the user can select one or multiple options from a predefined list (`options` and `suboptions`).

## Props

The component accepts standard `FormFieldProps` (`name`, `disabled`, `formik`) and a `config` object with the following properties:

| Name               | Type                                | Description                                                                                                | Required | Default      |
| :----------------- | :---------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :----------- |
| `fullWidth`        | `boolean`                           | If true, the element takes the full width of its container.                                                | No       | `false`      |
| `margin`           | `'dense' \| 'normal' \| 'none'`     | Margin around the control.                                                                                 | No       | `'normal'`   |
| `required`         | `boolean`                           | Marks the field as required (visual indicator might depend on `FormControl`).                              | No       | `false`      |
| `variant`          | `'standard' \| 'outlined' \| ...` | Visual style variant of the control.                                                                       | No       | `'standard'` |
| `paddingBottom`    | `'dense' \| 'normal' \| 'none'`     | Padding below the control.                                                                                 | No       | `undefined`  |
| `label`            | `string`                            | Label for the form element (may be used by `FormControl`).                                                 | No       | `''`         |
| `options`          | `OptionsItemShape[]`                | An array of primary options to be displayed in the sub-form.                                               | Yes      | `[]`         |
| `suboptions`       | `SubOptionsShape`                   | An object containing secondary options, often dependent on the primary selection.                          | No       | `undefined`  |
| `initialValue`     | `any`                               | The initial value of the form field.                                                                       | No       | `undefined`  |
| `disable_custom`   | `boolean`                           | If true, disables the ability to add custom options in the sub-form.                                       | No       | `false`      |
| `value_type`       | `string`                            | Specifies the data type of the value (e.g., 'string', 'number').                                           | No       | `undefined`  |
| `multiple`         | `boolean`                           | If true, allows multiple options to be selected in the sub-form.                                           | No       | `false`      |
| `enable_search`    | `boolean`                           | If true, enables a search input within the sub-form.                                                       | No       | `false`      |
| `disable_uncheck`  | `boolean`                           | If true, prevents users from deselecting an already selected option.                                       | No       | `false`      |
| `choice_type`      | `string`                            | Defines the selection mechanism in the sub-form (e.g., 'radio', 'checkbox').                               | No       | `undefined`  |
| `placeholder`      | `string`                            | Placeholder text, potentially shown when no value is selected or in the sub-form's search.                 | No       | `undefined`  |
| `showWithoutOptions`| `boolean`                           | If true, the element is rendered even when no `options` are provided.                                      | No       | `false`      |
| `useSectionList`   | `boolean`                           | If true, the sub-form uses a `SectionList` for displaying options, suitable for grouped data.              | No       | `false`      |
| `icon`             | `string`                            | The name of the Lineficon icon to display next to the selected value.                                      | Yes      | `''`         |
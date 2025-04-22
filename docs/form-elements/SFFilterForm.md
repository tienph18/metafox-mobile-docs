# SFFilterForm

Renders a button that opens a bottom sheet containing a sub-form, typically used for applying filters within a larger form. Pressing the button navigates to a dedicated screen (`FORM_BOTTOM_SHEET`) where the filter options, defined by the `options` and `suboptions` props, are presented.

## Props

| Name               | Type                  | Description                                                                 | Required   | Default     |
| :----------------- | :-------------------- | :-------------------------------------------------------------------------- | :--------- | :---------- |
| `fullWidth`        | `boolean`             | Determines if the control takes the full available width.                   | No         | `false`     |
| `margin`           | `normal` \| `dense` \| `none` | Sets the outer margin of the control.                                     | No         | `normal`    |
| `variant`          | `standard` \| `outlined` \| `filled` | The visual style variant of the control.                                  | No         | `standard`  |
| `paddingBottom`    | `normal` \| `dense` \| `none` | Sets the bottom padding of the control.                                   | No         | `normal`    |
| `label`            | `string`              | Label for the form control (not directly displayed on the button).          | No         | `undefined` |
| `suboptions`       | `SubOptionsShape`     | Configuration for the sub-form displayed in the bottom sheet.             | Yes        | `undefined` |
| `initialValue`     | `OptionsItemShape[]`  | Initial values for the filter options within the sub-form.                | No         | `undefined` |
| `disable_custom`   | `boolean`             | Disables custom options in the sub-form.                                  | No         | `false`     |
| `value_type`       | `string`              | Specifies the expected data type of the selected value(s) in the sub-form. | No         | `undefined` |
| `multiple`         | `boolean`             | Allows multiple selections in the sub-form.                               | No         | `false`     |
| `options`          | `OptionsItemShape[]`  | The list of options to display within the sub-form.                       | Yes        | `[]`        |
| `enable_search`    | `boolean`             | Enables a search input within the sub-form.                               | No         | `false`     |
| `disable_uncheck`  | `boolean`             | Prevents unselecting options once selected in the sub-form.               | No         | `false`     |
| `choice_type`      | `string`              | Specifies the type of choice input used in the sub-form (e.g., 'checkbox'). | No         | `undefined` |
| `placeholder`      | `string`              | Placeholder text (context might vary depending on sub-form implementation). | No         | `undefined` |
| `showWithoutOptions`| `boolean`             | Determines if the filter button should be shown even when no options exist. | No         | `false`     |
| `useSectionList`   | `boolean`             | Uses a `SectionList` for displaying options in the sub-form if true.      | No         | `false`     |
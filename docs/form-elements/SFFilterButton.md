# SFFilterButton

This form element renders a button, typically represented by an icon. When pressed, it opens a bottom sheet containing a sub-form (`ui.SubFormBuilder`) based on the main form's schema. This allows users to configure and apply filter criteria, which are then reflected in the main form's values upon submission of the sub-form.

## Props

| Name               | Type                   | Description                                                                 | Required | Default      |
| :----------------- | :--------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `fullWidth`        | `boolean`              | Determines if the element should occupy the full width of its container.    | No       | `false`      |
| `variant`          | `keyof typeof Variant` | Specifies the visual style variant (e.g., 'standard', 'outlined').          | No       | `'standard'` |
| `margin`           | `keyof typeof SizeEnum`  | Sets the margin size around the element.                                    | No       | `undefined`  |
| `required`         | `boolean`              | Indicates if a selection is required (validation handled in the sub-form).  | No       | `false`      |
| `paddingBottom`    | `keyof typeof SizeEnum`  | Sets the bottom padding size.                                             | No       | `undefined`  |
| `label`            | `string`               | Label text (primarily for accessibility or layout context).                 | No       | `''`         |
| `suboptions`       | `SubOptionsShape`      | Configuration for sub-options within the filter form.                       | No       | `undefined`  |
| `initialValue`     | `OptionsItemShape[]`   | Default selected values for the filter options.                             | No       | `undefined`  |
| `disable_custom`   | `boolean`              | If `true`, disables custom value input in the filter form.                  | No       | `false`      |
| `value_type`       | `string`               | Specifies the expected data type of the filter value.                       | No       | `undefined`  |
| `multiple`         | `boolean`              | If `true`, allows multiple selections in the filter form.                   | No       | `false`      |
| `options`          | `OptionsItemShape[]`   | The list of available options to display in the filter form.                | No       | `[]`         |
| `enable_search`    | `boolean`              | If `true`, enables a search input within the filter form options.           | No       | `false`      |
| `disable_uncheck`  | `boolean`              | If `true`, prevents users from unselecting an already selected option.      | No       | `false`      |
| `choice_type`      | `string`               | Defines the selection mechanism (e.g., 'radio', 'checkbox').                | No       | `undefined`  |
| `placeholder`      | `string`               | Placeholder text (likely used within the filter form, not the button).      | No       | `''`         |
| `showWithoutOptions`| `boolean`              | If `true`, the button is shown even when there are no `config.options`.     | No       | `false`      |
| `useSectionList`   | `boolean`              | If `true`, uses a `SectionList` component to render options in the filter form. | No       | `false`      |
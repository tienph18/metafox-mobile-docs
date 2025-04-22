# MultiChoice

The `MultiChoice` form element allows users to select one or multiple options from a predefined list, typically presented using checkboxes when multiple selections are allowed. It is functionally equivalent to the `Select` element but configured for multiple selections.

## Props

| Name               | Type                               | Description                                                                 | Required | Default      |
| :----------------- | :--------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `label`            | `string`                           | The text label displayed for the field.                                     | Yes      |              |
| `description`      | `string`                           | Additional descriptive text displayed below the field.                      | No       |              |
| `options`          | `OptionsItemShape[]`               | An array of available options to select from.                               | Yes      | `[]`         |
| `multiple`         | `boolean`                          | If true, allows selecting multiple options. Defaults to `true` for MultiChoice. | No       | `true`       |
| `required`         | `boolean`                          | Whether the field is required.                                              | No       | `false`      |
| `disabled`         | `boolean`                          | If true, disables the field.                                                | No       | `false`      |
| `variant`          | `'standard', 'outlined', 'filled'` | The visual style of the component.                                          | No       | `'standard'` |
| `margin`           | `'normal', 'dense', 'none'`        | Defines the margin size around the component.                               | No       | `'normal'`   |
| `fullWidth`        | `boolean`                          | If true, the component takes up the full width of its container.            | No       | `false`      |
| `placeholder`      | `string`                           | Placeholder text shown when no value is selected.                           | No       | `'select'`   |
| `enable_search`    | `boolean`                          | If true, enables a search input within the option selector modal.           | No       | `false`      |
| `disableClearable` | `boolean`                          | If true, prevents the user from clearing the selection (requires a value).  | No       | `false`      |
| `value_type`       | `string`                           | Specifies the expected data type of the value ('array' or single value).    | No       | `'array'`    |
| `suboptions`       | `SubOptionsShape`                  | Defines sub-options, often used for dependent selections.                   | No       | `undefined`  |
| `useSectionList`   | `boolean`                          | If true, uses a SectionList for displaying options (for grouped options).   | No       | `false`      |
| `showWithoutOptions`| `boolean`                          | If true, renders the component even if no options are provided.             | No       | `false`      |

*Note: `OptionsItemShape` typically has `{ label: string, value: string | number }` structure. `SubOptionsShape` structure depends on implementation.*
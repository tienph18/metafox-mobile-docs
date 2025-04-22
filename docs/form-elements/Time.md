# Time

A form element that allows users to select a specific time using a native time picker interface. This element is an alias for the `Date` element, configured specifically for time selection.

## Props

| Name             | Type                                       | Description                                                                 | Required | Default                  |
|------------------|--------------------------------------------|-----------------------------------------------------------------------------|----------|--------------------------|
| `label`          | `string`                                   | The label displayed for the time input.                                     | Yes      | -                        |
| `description`    | `string`                                   | Optional help text displayed below the input.                               | No       | `undefined`              |
| `placeholder`    | `string`                                   | Placeholder text shown when the input is empty.                             | No       | `undefined`              |
| `displayFormat`  | `string`                                   | The format used to display the selected time (e.g., 'HH:mm', 'h:mm A').     | No       | `'HH:mm'` (Recommended)  |
| `resultFormat`   | `string`                                   | The format the selected time is stored in. Defaults to ISO 8601 format if unset. | No       | ISO 8601 String        |
| `timeFormat`     | `12 \| 24`                               | Specifies whether to use 12-hour or 24-hour format in the picker.         | No       | Locale default           |
| `initialValue`   | `string`                                   | An initial time value for the field (must match resultFormat if specified, otherwise ISO 8601). | No       | `undefined`              |
| `disabled`       | `boolean`                                  | If `true`, the input field is disabled.                                     | No       | `false`                  |
| `required`       | `boolean`                                  | If `true`, the field must have a value.                                     | No       | `false`                  |
| `fullWidth`      | `boolean`                                  | If `true`, the element spans the full width of its container.               | No       | `false`                  |
| `margin`         | `'none' \| 'dense' \| 'normal'`            | Sets the outer margin of the form control.                                  | No       | `'normal'`               |
| `variant`        | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | The visual style variant of the input.                                      | No       | `'standard'`             |
| `time_zone_gmt`  | `string`                                   | Timezone identifier (e.g., 'UTC', 'America/New_York') for display formatting. | No       | User's current timezone |

**Note:** This element utilizes the `DatePickerField` component internally with its `datePickerMode` prop implicitly set to `'time'`. Props like `minDate`, `maxDate`, `startOfDay`, and `endOfDay` from `DatePickerField` are technically available but may have limited relevance or unexpected behavior in a time-only context.
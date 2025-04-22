# SFDatetime

A form input element that allows users to select a date, time, or both using a native modal picker. It displays the selected value in a formatted text input. This element is an alias for `SFDate` but typically configured with `datePickerMode: 'datetime'`.

## Props

| Name             | Type                      | Description                                                                                             | Required | Default                  |
| :--------------- | :------------------------ | :------------------------------------------------------------------------------------------------------ | :------- | :----------------------- |
| `label`          | `string`                  | The label text for the input field (can be a translation key).                                          | Yes      | `'close_time'`           |
| `placeholder`    | `string`                  | Placeholder text shown when the input is empty.                                                         | Yes      | -                        |
| `datePickerMode` | `'date'\|'time'\|'datetime'` | Determines if the picker selects date, time, or both.                                           | Yes      | `'datetime'`             |
| `displayFormat`  | `string`                  | Moment.js format for displaying the selected date/time in the input.                                    | Yes      | `'DD/MM/YYYY - HH:mm'`   |
| `required`       | `boolean`                 | Marks the field as required for form validation.                                                        | Yes      | `false`                  |
| `disabled`       | `boolean`                 | Disables the input field.                                                                               | No       | `false`                  |
| `variant`        | `'standard'\|'outlined'\|...` | The visual style variant of the input.                                                                  | Yes      | `'standard'`             |
| `fullWidth`      | `boolean`                 | If true, the component takes up the full width of its container.                                        | No       | `false`                  |
| `margin`         | `'none'\|'dense'\|'normal'` | Controls the margin around the component.                                                               | Yes      | `'normal'` (assumed)     |
| `minDate`        | `string`                  | Minimum selectable date (ISO 8601 format).                                                              | No       | -                        |
| `maxDate`        | `string`                  | Maximum selectable date (ISO 8601 format).                                                              | No       | -                        |
| `time_zone_gmt`  | `string`                  | IANA time zone name (e.g., 'Asia/Saigon') for date calculations. Defaults to device timezone if omitted. | Yes      | Device Timezone          |
| `timeFormat`     | `12 \| 24`                | Use 12-hour or 24-hour format in the time picker.                                                       | No       | System Default           |
| `startOfDay`     | `boolean`                 | Set selected date's value to the start of the day (00:00:00).                                           | No       | `false`                  |
| `endOfDay`       | `boolean`                 | Set selected date's value to the end of the day (23:59:59).                                             | No       | `false`                  |
| `editable`       | `boolean`                 | If false, prevents direct text input, forcing picker use.                                               | No       | `true`                   |

*Note: `required` status is based on the TypeScript `Config` type definition. Default values are inferred from code logic where possible.*
# Datetime

The same with element Date.

## Props

Props are configured via the `config` object passed to the component.

| Name             | Type                             | Description                                                                 | Required | Default             |
| :--------------- | :------------------------------- | :-------------------------------------------------------------------------- | :------- | :------------------ |
| `label`          | `string`                         | The text label displayed for the field.                                     | No       | `'close_time'`      |
| `description`    | `string`                         | Help text displayed below the input field.                                  | No       |                     |
| `placeholder`    | `string`                         | The placeholder text shown when the input is empty.                         | No       |                     |
| `datePickerMode` | `'date' \| 'time' \| 'datetime'` | Determines if the picker selects date, time, or both.                       | No       | `'datetime'`        |
| `displayFormat`  | `string`                         | The Moment.js format string used to display the selected value.             | No       | `'DD/MM/YYYY - HH:mm'` |
| `initialValue`   | `string`                         | An initial value for the date/time field (ISO 8601 format recommended).     | No       |                     |
| `minDate`        | `string`                         | The minimum selectable date (format depends on `momentResultFormat`).       | No       |                     |
| `maxDate`        | `string`                         | The maximum selectable date (format depends on `momentResultFormat`).       | No       |                     |
| `momentResultFormat` | `string`                     | The Moment.js format string used for parsing `minDate` and `maxDate`.       | No       |                     |
| `time_zone_gmt`  | `string`                         | The timezone identifier (e.g., 'America/New_York') used for formatting.     | No       |                     |
| `timeFormat`     | `12 \| 24`                       | Specifies 12-hour or 24-hour time format for the picker.                    | No       | (Locale default)    |
| `startOfDay`     | `boolean`                        | If true, sets the selected date's time to the start of the day (00:00:00).  | No       | `false`             |
| `endOfDay`       | `boolean`                        | If true, sets the selected date's time to the end of the day (23:59:59).    | No       | `false`             |
| `required`       | `boolean`                        | Whether the field is mandatory.                                             | No       | `false`             |
| `disabled`       | `boolean`                        | Disables the input field.                                                   | No       | `false`             |
| `fullWidth`      | `boolean`                        | If true, the component takes up the full width of its container.            | No       | `false`             |
| `margin`         | `'none' \| 'dense' \| 'normal'`  | Controls the margin around the component.                                   | No       | `'normal'`          |
| `paddingBottom`  | `'none' \| 'dense' \| 'normal'`  | Controls the bottom padding of the component.                               | No       | `'normal'`          |
| `variant`        | `'standard' \| 'outlined' \| 'filled'` | The visual style of the input field.                                        | No       | `'standard'`        |

*Note: The component also accepts standard `FormFieldProps` like `name` (required) and `formik` (required), as well as top-level `disabled` and `required` props that can override the corresponding settings within `config`.*
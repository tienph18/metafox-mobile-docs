# SFDate

A form element that allows users to select a date, time, or both using a native modal picker. It displays the selected value in a specified format.

## Props

| Name               | Type                         | Description                                                                              | Required | Default             |
|--------------------|------------------------------|------------------------------------------------------------------------------------------|----------|---------------------|
| `fullWidth`        | `boolean`                    | Controls if the element takes the full width.                                            | No       | `false`             |
| `margin`           | `'none' \| 'dense' \| 'normal'` | Margin spacing around the element.                                                       | No       | `'normal'`          |
| `paddingBottom`    | `'none' \| 'dense' \| 'normal'` | Bottom padding below the element.                                                        | No       | `'none'`            |
| `variant`          | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the input field.                                             | No       | `'standard'`        |
| `time_zone_gmt`    | `string`                     | The GMT timezone string (e.g., 'Asia/Ho_Chi_Minh') for date calculations.                | No       | `undefined`         |
| `label`            | `string`                     | The label text displayed for the field.                                                  | No       | `'close_time'`      |
| `placeholder`      | `string`                     | Placeholder text shown when no value is selected.                                        | No       | `undefined`         |
| `required`         | `boolean`                    | Marks the field as mandatory.                                                            | No       | `false`             |
| `editable`         | `boolean`                    | If `false`, the text input part is not directly editable (picker still works).           | No       | `true`              |
| `minDate`          | `string`                     | The minimum selectable date/time (ISO 8601 format or format specified by `momentResultFormat`). | No       | `undefined`         |
| `maxDate`          | `string`                     | The maximum selectable date/time (ISO 8601 format or format specified by `momentResultFormat`). | No       | `undefined`         |
| `momentResultFormat`| `string`                     | The Moment.js format string used for parsing `minDate` and `maxDate`.                    | No       | `undefined`         |
| `datePickerMode`   | `'date' \| 'time' \| 'datetime'` | Determines if the picker allows selecting date, time, or both.                           | No       | `'datetime'`        |
| `displayFormat`    | `string`                     | The Moment.js format string for displaying the selected value in the input field.        | No       | `'DD/MM/YYYY - HH:mm'`|
| `initialValue`     | `string`                     | The initial value for the date picker (ISO 8601 format).                                 | No       | `undefined`         |
| `timeFormat`       | `12 \| 24`                   | Specifies 12 or 24-hour time format for the time picker.                                 | No       | `12`                |
| `startOfDay`       | `boolean`                    | If true, sets the selected date's time to the start of the day (00:00:00).               | No       | `false`             |
| `endOfDay`         | `boolean`                    | If true, sets the selected date's time to the end of the day (23:59:59).                 | No       | `false`             |

# Date

A form element that allows users to select a date, time, or both using a native modal picker.

## Props

| Name           | Type                             | Description                                                                 | Required | Default             |
| -------------- | -------------------------------- | --------------------------------------------------------------------------- | -------- | ------------------- |
| label          | string                           | The text label displayed for the field.                                     | Yes      | `'close_time'`      |
| placeholder    | string                           | Placeholder text for the input field.                                       | No       |                     |
| description    | string                           | Additional descriptive text displayed below the input.                      | No       |                     |
| required       | boolean                          | Whether the field is mandatory.                                             | No       | `false`             |
| disabled       | boolean                          | Whether the field is disabled and cannot be interacted with.                | No       | `false`             |
| fullWidth      | boolean                          | If `true`, the component takes up the full width of its container.          | No       | `false`             |
| margin         | `'none' \| 'normal' \| 'dense'`  | Defines the margin spacing around the component.                            | No       | `'normal'`          |
| variant        | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the input field.                              | No       | `'standard'`        |
| datePickerMode | `'date' \| 'time' \| 'datetime'` | Determines if the picker selects date, time, or both.                     | No       | `'datetime'`        |
| displayFormat  | string                           | The `moment.js` format string used to display the selected date/time.     | No       | `'DD/MM/YYYY - HH:mm'` |
| minDate        | string                           | The minimum selectable date (ISO string or format specified by `momentResultFormat`). | No       |                     |
| maxDate        | string                           | The maximum selectable date (ISO string or format specified by `momentResultFormat`). | No       |                     |
| time_zone_gmt  | string                           | Timezone identifier (e.g., 'Asia/Ho_Chi_Minh') for display formatting.    | No       | User's timezone     |
| timeFormat     | `12 \| 24`                       | Specifies 12 or 24-hour time format for the picker.                       | No       | `12`                |
| startOfDay     | boolean                          | If `true`, sets the selected time to the start of the day (00:00:00).     | No       | `false`             |
| endOfDay       | boolean                          | If `true`, sets the selected time to the end of the day (23:59:59).       | No       | `false`             |
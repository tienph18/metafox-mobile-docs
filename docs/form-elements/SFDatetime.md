## SFDatetime

A form input element that allows users to select a date, time, or both using a native modal picker. It displays the selected value in a formatted text input. This element is an alias for `SFDate` but typically configured with `datePickerMode: 'datetime'`.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `datePickerMode` | `'date'\|'time'\|'datetime'` | Determines if the picker selects date, time, or both. | Yes | `'datetime'` |
| `disabled` | `boolean` | | | `false` |
| `displayFormat` | `string` | Moment.js format for displaying the selected date/time in the input. | Yes | `'DD/MM/YYYY - HH:mm'` |
| `editable` | `boolean` | If false, prevents direct text input, forcing picker use. | | `true` |
| `endOfDay` | `boolean` | Set selected date's value to the end of the day (23:59:59). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | `'close_time'` |
| `margin` | `'none'\|'dense'\|'normal'` | | Yes | `'normal'` |
| `maxDate` | `string` | Maximum selectable date (ISO 8601 format). | | |
| `minDate` | `string` | Minimum selectable date (ISO 8601 format). | | |
| `placeholder` | `string` | | Yes | |
| `required` | `boolean` | | Yes | `false` |
| `startOfDay` | `boolean` | Set selected date's value to the start of the day (00:00:00). | | `false` |
| `time_zone_gmt` | `string` | IANA time zone name (e.g., 'Asia/Saigon') for date calculations. Defaults to device timezone if omitted. | Yes | Device Timezone |
| `timeFormat` | `12 \| 24` | Use 12-hour or 24-hour format in the time picker. | | System Default |
| `variant` | `'standard'\|'outlined'\|...` | Specifies the visual style of the component. | Yes | `'standard'` |

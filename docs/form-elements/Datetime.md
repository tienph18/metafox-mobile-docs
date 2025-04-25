## Datetime

The same with element Date.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `datePickerMode` | `'date' \| 'time' \| 'datetime'` | Determines if the picker selects date, time, or both. | | `'datetime'` |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `displayFormat` | `string` | The Moment.js format string used to display the selected value. | | `'DD/MM/YYYY - HH:mm'` |
| `endOfDay` | `boolean` | If true, sets the selected date's time to the end of the day (23:59:59). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `string` | An initial value for the date/time field (ISO 8601 format recommended). | | |
| `label` | `string` | | | `'close_time'` |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `maxDate` | `string` | The maximum selectable date (format depends on `momentResultFormat`). | | |
| `minDate` | `string` | The minimum selectable date (format depends on `momentResultFormat`). | | |
| `momentResultFormat` | `string` | The Moment.js format string used for parsing `minDate` and `maxDate`. | | |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `placeholder` | `string` | | | |
| `required` | `boolean` | | | `false` |
| `startOfDay` | `boolean` | If true, sets the selected date's time to the start of the day (00:00:00). | | `false` |
| `time_zone_gmt` | `string` | The timezone identifier (e.g., 'America/New_York') used for formatting. | | |
| `timeFormat` | `12 \| 24` | Specifies 12-hour or 24-hour time format for the picker. | | (Locale default) |
| `variant` | `'standard' \| 'outlined' \| 'standard-outlined' \| 'outlined-inlined'` | Specifies the visual style of the component. | | `'standard'` |

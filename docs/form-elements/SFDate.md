## SFDate

A form element that allows users to select a date, time, or both using a native modal picker. It displays the selected value in a specified format.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `datePickerMode` | `'date' \| 'time' \| 'datetime'` | Determines if the picker allows selecting date, time, or both. | | `'datetime'` |
| `displayFormat` | `string` | The Moment.js format string for displaying the selected value in the input field. | | `'DD/MM/YYYY - HH:mm'` |
| `editable` | `boolean` | If `false`, the text input part is not directly editable (picker still works). | | `true` |
| `endOfDay` | `boolean` | If true, sets the selected date's time to the end of the day (23:59:59). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `string` | The initial value for the date picker (ISO 8601 format). | | `undefined` |
| `label` | `string` | | | `'close_time'` |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `maxDate` | `string` | The maximum selectable date/time (ISO 8601 format or format specified by `momentResultFormat`). | | `undefined` |
| `minDate` | `string` | The minimum selectable date/time (ISO 8601 format or format specified by `momentResultFormat`). | | `undefined` |
| `momentResultFormat` | `string` | The Moment.js format string used for parsing `minDate` and `maxDate`. | | `undefined` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `'none'` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `startOfDay` | `boolean` | If true, sets the selected date's time to the start of the day (00:00:00). | | `false` |
| `time_zone_gmt` | `string` | The GMT timezone string (e.g., 'Asia/Ho_Chi_Minh') for date calculations. | | `undefined` |
| `timeFormat` | `12 \| 24` | Specifies 12 or 24-hour time format for the time picker. | | `12` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

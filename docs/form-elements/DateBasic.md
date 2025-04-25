## DateBasic

A form element component that provides a user interface for selecting a date, time, or datetime using a native modal picker. It integrates with Formik for form state management.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `datePickerMode` | `'date' \| 'time' \| 'datetime'` | Determines the type of picker shown (`date`, `time`, or `datetime`). | | `'date'` |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | If `false`, the text input part is not directly editable by the user. | | `true` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `string` | An initial value to populate the date field with. | | `undefined` |
| `label` | `string` | | | `'close_time'` |
| `margin` | `string` | | | `normal` |
| `maxDate` | `string` | The latest selectable date (format defined by `momentResultFormat`). | | `undefined` |
| `minDate` | `string` | The earliest selectable date (format defined by `momentResultFormat`). | | `undefined` |
| `momentResultFormat` | `string` | The Moment.js format string used for parsing `minDate` and `maxDate`. | | `''` |
| `paddingBottom` | `string` | | | `normal` |
| `placeholder` | `string` | | | `''` |
| `required` | `boolean` | | | `false` |
| `resultFormat` | `string` | The desired format for the final value submitted by the form. | | `''` |
| `time_zone_gmt` | `string` | Specifies the GMT timezone offset (e.g., "+07:00"). | | `''` |
| `timeFormat` | `number` | Specifies the time format (e.g., `12` or `24` for 12/24 hour format). | | `12` |
| `valueFormat` | `string` | The Moment.js format string for displaying and storing the selected value. | | `'DD/MM/YYYY'` |
| `variant` | `'standard' \| 'outlined' \| 'standard-outlined' \| 'outlined-inlined'` | Specifies the visual style of the component. | | `'standard'` |

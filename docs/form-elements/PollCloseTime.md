# PollCloseTime

This element renders a date and time picker input field, specifically configured for selecting the closing time of a poll. It utilizes the underlying `DatePickerField` component.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `label` | `string` | The text label displayed for the input field. | | `'close_time'` |
| `placeholder` | `string` | Placeholder text shown when the input is empty. | | |
| `description` | `string` | Additional descriptive text displayed below the input field. | | |
| `required` | `boolean` | If true, the field must have a value for form submission. | | `false` |
| `disabled` | `boolean` | If true, the input field is disabled and cannot be interacted with. | | `false` |
| `fullWidth` | `boolean` | If true, the input field spans the full width of its container. | | `false` |
| `margin` | `'dense'`, `'normal'`, `'none'` | Specifies the margin spacing around the field. | | `'normal'` |
| `variant` | `'standard'`, `'outlined'`, `'filled'` | Defines the visual style of the input field. | | `'standard'` |
| `datePickerMode` | `'date'`, `'time'`, `'datetime'` | Determines the type of picker displayed (date, time, or both). | | `'datetime'` |
| `displayFormat` | `string` | The format used to display the selected date and time in the input field. | | `'DD/MM/YYYY - HH:mm'` |
| `minDate` | `string` | The earliest selectable date/time (ISO 8601 format string). | | |
| `maxDate` | `string` | The latest selectable date/time (ISO 8601 format string). | | |
| `time_zone_gmt` | `string` | Timezone identifier (e.g., 'America/New_York') for calculations. | | User's setting |
| `timeFormat` | `12`, `24` | Specifies whether to use 12-hour or 24-hour format in the time picker. | | User's setting |
| `startOfDay` | `boolean` | If true, sets the selected time to the beginning of the day (00:00:00). | | `false` |
| `endOfDay` | `boolean` | If true, sets the selected time to the end of the day (23:59:59). | | `false` |
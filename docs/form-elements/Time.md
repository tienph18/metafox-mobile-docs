## Time

*Note: This element inherits most props from the base `Date` element.*

For a visual reference, see [Date Gallery](./form-elements/Date.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `undefined` |
| `disabled` | `boolean` | | | `false` |
| `displayFormat` | `string` | The format used to display the selected time (e.g., 'HH:mm', 'h:mm A'). | | `'HH:mm'` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `string` | An initial time value for the field (must match resultFormat if specified, otherwise ISO 8601). | | `undefined` |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `resultFormat` | `string` | The format the selected time is stored in. Defaults to ISO 8601 format if unset. | | ISO 8601 String |
| `time_zone_gmt` | `string` | Timezone identifier (e.g., 'UTC', 'America/New_York') for display formatting. | | User's current timezone |
| `timeFormat` | `12 \| 24` | Specifies whether to use 12-hour or 24-hour format in the picker. | | Locale default |
| `variant` | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

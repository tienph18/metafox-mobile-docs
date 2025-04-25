## input

*Note: This element inherits most props from the base `Text` element.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none'`, `'sentences'`, `'words'`, `'characters'` | Auto-capitalization behavior. | | `'sentences'` |
| `autoCorrect` | `boolean` | Enable/disable auto-correction. | | `true` |
| `autoFocus` | `boolean` | | | `false` |
| `backgroundColor` | `string` | Background color for the input container. | | |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls when the clear button appears (iOS only). | | `'never'` |
| `contextualDescription` | `string` | Additional description text, often used with `findReplace`. | | |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | If false, the text is not editable (overridden by `disabled`). | | `true` |
| `label` | `string` | | | `'close_time'` |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | `'normal'` |
| `maxDate` | `string` | The latest selectable date/time (ISO 8601 format string). | | |
| `minDate` | `string` | The earliest selectable date/time (ISO 8601 format string). | | |
| `placeholder` | `string` | | | |
| `required` | `boolean` | | | `false` |
| `startOfDay` | `boolean` | If `true`, sets the selected time to the beginning of the day (00:00:00). | | `false` |
| `time_zone_gmt` | `string` | Timezone identifier (e.g., 'America/New_York') for calculations. | | User's setting |
| `timeFormat` | `12 \| 24` | Specifies whether to use 12-hour or 24-hour format in the time picker. | | User's setting |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

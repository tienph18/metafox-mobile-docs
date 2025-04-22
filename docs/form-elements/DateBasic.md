# DateBasic

A form element component that provides a user interface for selecting a date, time, or datetime using a native modal picker. It integrates with Formik for form state management.

## Props

| Name               | Type                           | Description                                                                 | Required | Default        |
| :----------------- | :----------------------------- | :-------------------------------------------------------------------------- | :------- | :------------- |
| `fullWidth`        | `boolean`                      | If `true`, the component stretches to the full width of its container.      | No       | `false`        |
| `margin`           | `string`                       | Sets the outer margin spacing for the component (`none`, `dense`, `normal`). | No       | `normal`       |
| `paddingBottom`    | `string`                       | Sets the bottom padding spacing (`none`, `dense`, `normal`).                | No       | `normal`       |
| `variant`          | `string`                       | The visual style variant (`standard`, `outlined`, `filled`).                | No       | `standard`     |
| `time_zone_gmt`    | `string`                       | Specifies the GMT timezone offset (e.g., "+07:00").                         | No       | `''`           |
| `label`            | `string`                       | The text label displayed above or alongside the input field.                | No       | `'close_time'` |
| `placeholder`      | `string`                       | Placeholder text displayed when the input field is empty.                   | No       | `''`           |
| `required`         | `boolean`                      | If `true`, the field is marked as mandatory in the form.                    | No       | `false`        |
| `editable`         | `boolean`                      | If `false`, the text input part is not directly editable by the user.       | No       | `true`         |
| `minDate`          | `string`                       | The earliest selectable date (format defined by `momentResultFormat`).      | No       | `undefined`    |
| `maxDate`          | `string`                       | The latest selectable date (format defined by `momentResultFormat`).        | No       | `undefined`    |
| `momentResultFormat` | `string`                       | The Moment.js format string used for parsing `minDate` and `maxDate`.       | No       | `''`           |
| `datePickerMode`   | `'date' \| 'time' \| 'datetime'` | Determines the type of picker shown (`date`, `time`, or `datetime`).        | No       | `'date'`       |
| `resultFormat`     | `string`                       | The desired format for the final value submitted by the form.               | No       | `''`           |
| `valueFormat`      | `string`                       | The Moment.js format string for displaying and storing the selected value.  | No       | `'DD/MM/YYYY'` |
| `initialValue`     | `string`                       | An initial value to populate the date field with.                           | No       | `undefined`    |
| `timeFormat`       | `number`                       | Specifies the time format (e.g., `12` or `24` for 12/24 hour format).       | No       | `12`           |
| `disabled`         | `boolean`                      | If `true`, the entire component is disabled and cannot be interacted with.  | No       | `false`        |
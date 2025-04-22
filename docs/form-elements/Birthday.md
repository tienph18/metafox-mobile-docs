# Birthday

The `Birthday` element provides a user-friendly interface for selecting a date, specifically intended for capturing a user's date of birth. It utilizes a native date picker interface.

## Props

| Name             | Type                             | Description                                                                 | Required | Default        |
| :--------------- | :------------------------------- | :-------------------------------------------------------------------------- | :------- | :------------- |
| `label`          | `string`                         | Text label displayed above the input field.                                 | No       | -              |
| `placeholder`    | `string`                         | Placeholder text shown when the input is empty.                             | No       | -              |
| `required`       | `boolean`                        | Specifies if the birthday field must be filled.                             | No       | `false`        |
| `disabled`       | `boolean`                        | Disables user interaction with the date picker.                             | No       | `false`        |
| `description`    | `string`                         | Additional helper text displayed below the input.                           | No       | -              |
| `fullWidth`      | `boolean`                        | If `true`, the element expands to the full width of its container.          | No       | `false`        |
| `margin`         | `'none' \| 'normal' \| 'dense'` | Controls the margin spacing around the element.                             | No       | `'normal'`     |
| `variant`        | `'standard' \| 'outlined' \| 'filled'` | Defines the visual style of the input field.                              | No       | `'standard'`   |
| `minDate`        | `string`                         | The earliest selectable date in ISO 8601 format (e.g., "1900-01-01").       | No       | -              |
| `maxDate`        | `string`                         | The latest selectable date in ISO 8601 format (e.g., "2024-12-31").         | No       | Current Date   |
| `initialValue`   | `string`                         | Sets the initial date displayed in ISO 8601 format.                         | No       | -              |
| `displayFormat`  | `string`                         | The format (using moment.js tokens) to display the selected date.         | No       | Locale default |

**Note:** This component internally uses a date picker (`DatePickerField`). While the underlying component supports time selection (`datePickerMode`), the `Birthday` element is intended for date selection only. The `maxDate` prop should typically be configured to prevent selecting future dates for birthdays.
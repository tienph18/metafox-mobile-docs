# NumberCode

A form input element designed for entering numerical codes (like One-Time Passwords) digit by digit into separate input boxes.

## Props

| Name                  | Type                                | Description                                                    | Required | Default      |
| :-------------------- | :---------------------------------- | :------------------------------------------------------------- | :------- | :----------- |
| `label`               | `string`                            | The label displayed above the input fields.                    | No       | `undefined`  |
| `editable`            | `boolean`                           | Determines if the input fields are editable.                   | No       | `true`       |
| `variant`             | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the form control.                  | No       | `'standard'` |
| `paddingBottom`       | `'dense' \| 'normal' \| 'none'`     | Controls the bottom padding of the form control.               | No       | `'dense'`    |
| `margin`              | `'dense' \| 'normal' \| 'none'`     | Controls the margin of the form control.                       | No       | `undefined`  |
| `required`            | `boolean`                           | If true, marks the field as required.                          | No       | `false`      |
| `fullWidth`           | `boolean`                           | If true, the component stretches to the full width available.  | No       | `false`      |
| `clearInputs`         | `boolean`                           | Controls input clearing behavior on press.                     | No       | `false`      |
| `isAutoFillSupported` | `boolean`                           | Enables native OTP autofill support if available.              | No       | `false`      |
| `isAutoFocus`         | `boolean`                           | If true, the first input box automatically receives focus.     | No       | `false`      |
| `codeLength`          | `number`                            | The number of digits/input boxes for the code.                 | No       | `6`          |
| `keyboardType`        | `TextInputProps['keyboardType']`    | Specifies the type of keyboard to display (e.g., 'numeric'). | No       | `'numeric'`  |
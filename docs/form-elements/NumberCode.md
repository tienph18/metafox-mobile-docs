# NumberCode

A form input element designed for entering numerical codes (like One-Time Passwords) digit by digit into separate input boxes.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `label` | `string` | The label displayed above the input fields. | | `undefined` |
| `editable` | `boolean` | Determines if the input fields are editable. | | `true` |
| `variant` | `'standard', 'outlined', 'filled'` | The visual style variant of the form control. | | `'standard'` |
| `paddingBottom` | `'dense', 'normal', 'none'` | Controls the bottom padding of the form control. | | `'dense'` |
| `margin` | `'dense', 'normal', 'none'` | Controls the margin of the form control. | | `undefined` |
| `required` | `boolean` | If true, marks the field as required. | | `false` |
| `fullWidth` | `boolean` | If true, the component stretches to the full width available. | | `false` |
| `clearInputs` | `boolean` | Controls input clearing behavior on press. | | `false` |
| `isAutoFillSupported` | `boolean` | Enables native OTP autofill support if available. | | `false` |
| `isAutoFocus` | `boolean` | If true, the first input box automatically receives focus. | | `false` |
| `codeLength` | `number` | The number of digits/input boxes for the code. | | `6` |
| `keyboardType` | `TextInputProps['keyboardType']` | Specifies the type of keyboard to display (e.g., 'numeric'). | | `'numeric'` |
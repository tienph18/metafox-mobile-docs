# Password

The `Password` element provides a secure text input field specifically designed for entering passwords. It includes a toggle button to show or hide the entered password for user convenience. It integrates with Formik for form state management.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `label` | `string` | The label displayed above or alongside the input field. | | `''` |
| `placeholder` | `string` | Placeholder text shown when the input field is empty. | | `''` |
| `required` | `boolean` | Marks the field as mandatory, often visually indicated (e.g., with an asterisk). | | `false` |
| `disabled` | `boolean` | If true, the input field is disabled and cannot be interacted with. | | `false` |
| `variant` | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'` | Defines the visual style of the input field (e.g., border, background). | | `'standard'` |
| `margin` | `'none'`, `'dense'`, `'normal'` | Controls the outer spacing around the form control. | | `'normal'` |
| `fullWidth` | `boolean` | If true, the component stretches to the full width of its container. | | `false` |
| `editable` | `boolean` | If false, the text content cannot be modified by the user. | | `true` |
| `returnKeyType` | `ReturnKeyTypeOptions` | Specifies the appearance of the keyboard's return key. | | `'next'` |
| `inputWapperStyle` | `ViewStyle` | Custom styles applied to the wrapper view containing the `TextInput`. | | `undefined` |
| `containerStyle` | `ViewStyle` | Custom styles applied to the outermost container of the component. | | `undefined` |
| `styleLabel` | `ViewStyle` | Custom styles applied specifically to the label text component. | | `undefined` |

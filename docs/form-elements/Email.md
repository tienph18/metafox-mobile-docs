## Email

*Note: This element inherits most props from the base `Text` element.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `...rest` | `TextInputProps` | Other standard React Native `TextInput` props are accepted. | | `undefined` |
| `autoCapitalize` | `'none'`, `'sentences'`, `'words'`, `'characters'` | How to automatically capitalize text. For Email, defaults to 'none'. | | `'none'` |
| `autoFocus` | `boolean` | | | `false` |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | When to display the clear text button (iOS only). | | `'never'` |
| `description` | `string` | | | `undefined` |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `keyboardType` | `string` | Determines which keyboard to open (e.g., 'numeric', 'email-address'). For Email, defaults to 'email-address'. | | `'email-address'` |
| `label` | `string` | | | `undefined` |
| `margin` | `'normal'`, `'dense'`, `'none'` | | | `'normal'` |
| `maxLength` | `number` | | | `undefined` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `returnKeyType` | `string` | Determines how the return key should look. | | `'default'` |
| `textContentType` | `string` | Give the keyboard and the system information about the expected semantic meaning for the content. For Email, defaults to 'emailAddress'. | | `'emailAddress'` |
| `validateAction` | `string` | Name of a registered action for backend validation on blur. | | `undefined` |
| `variant` | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

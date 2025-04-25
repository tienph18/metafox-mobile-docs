## question

*Note: This element inherits most props from the base `Text` element.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none'`, `'sentences'`, `'words'`, `'characters'` | Controls how text input is automatically capitalized. | | `'sentences'` |
| `autoCorrect` | `boolean` | Controls whether autocorrection should be enabled. | | `true` |
| `autoFocus` | `boolean` | | | `false` |
| `backgroundColor` | `string` | Sets a custom background color for the input field. | | |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls when the standard clear button appears in the text field (iOS only). | | `'never'` |
| `contextualDescription` | `string` | Additional description shown below the input, often used for dynamic info. | | |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | If `false`, the text field value cannot be changed. | | `true` |
| `findReplace` | `{ find: string, replace: string }` | Configuration to display a transformed version of the input (e.g., slug). | | |
| `fullWidth` | `boolean` | | | `false` |
| `hasCopy` | `boolean` | If `true`, displays a copy-to-clipboard icon button. | | `false` |
| `hasQRScanner` | `boolean` | If `true`, displays a QR code scanner icon button. | | `false` |
| `keyboardType` | `string` | Specifies the type of keyboard to display (e.g., 'numeric', 'email-address'). | | `'default'` |
| `label` | `string` | | | |
| `margin` | `'normal'`, `'dense'`, `'none'` etc. | | | `'normal'` |
| `maxLength` | `number` | | | |
| `minHeight` | `number` | | | |
| `multiline` | `boolean` | If `true`, allows multiple lines of text input. | | `false` |
| `paddingBottom` | `'normal'`, `'dense'`, `'none'` etc. | | | |
| `placeholder` | `string` | | | |
| `qrScannerParamName` | `string` | The URL query parameter name to extract when using the QR scanner. | | `'invite_code'` |
| `required` | `boolean` | | | `false` |
| `returnKeyType` | `string` | Specifies the appearance of the return key (e.g., 'done', 'next'). | | `'done'` |
| `secureTextEntry` | `boolean` | If `true`, masks the text entered (for passwords). | | `false` |
| `validateAction` | `string` | Name of a resource action used for asynchronous backend validation on blur. | | |
| `variant` | `'standard'`, `'outlined'`, `'filled'`, `'livestream'` etc. | Specifies the visual style of the component. | | `'standard'` |

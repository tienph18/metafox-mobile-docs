## Text

A standard text input field for forms, allowing users to enter single or multiple lines of text.


### Variants

**Standard**
![Standard variant](/assets/Text/standard.png)

**Standard Inlined**
![Standard Inlined variant](/assets/Text/standard-inlined.png)

**Standard Outlined**
![Standard Outlined variant](/assets/Text/standard-outlined.png)

**Outlined**
![Outlined variant](/assets/Text/outlined.png)


### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none' \| 'sentences' \| 'words' \| 'characters'` | Controls automatic capitalization behavior. | | `'sentences'` |
| `autoCorrect` | `boolean` | Enables or disables auto-correction for the input. | | `true` |
| `autoFocus` | `boolean` | | | `false` |
| `backgroundColor` | `string` | Sets the background color for the input wrapper. | | |
| `clearButtonMode` | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | (iOS only) When to display the clear text button. | | `'never'` |
| `contextualDescription` | `string` | Additional descriptive text displayed near the input. | | |
| `description` | `string` | | | |
| `editable` | `boolean` | If `false`, the text input is not editable. | | `true` |
| `findReplace` | `{ find: string, replace: string }` | Configuration to automatically generate a slug-like value based on input. | | |
| `fullWidth` | `boolean` | | | `false` |
| `hasCopy` | `boolean` | If `true`, displays a copy-to-clipboard icon button. | | `false` |
| `hasQRScanner` | `boolean` | If `true`, displays a QR code scanner icon button. | | `false` |
| `label` | `string` | | | |
| `margin` | `'none' \| 'normal' \| 'dense'` | | | `'normal'` |
| `maxLength` | `number` | | | |
| `minHeight` | `number` | | | |
| `multipleline` | `boolean` | If `true`, allows multiple lines of text input (textarea). | | `false` |
| `placeholder` | `string` | | | |
| `qrScannerParamName` | `string` | Query parameter name to extract from the scanned QR code URL. | | `'invite_code'` |
| `required` | `boolean` | | | `false` |
| `validateAction` | `string` | Name of a registered action for backend validation triggered on blur. | | |
| `variant` | `'standard' \| 'standard-inlined' \| 'standard-outlined' \| 'outlined'` | The visual style variant of the input field. | | `'standard'` |

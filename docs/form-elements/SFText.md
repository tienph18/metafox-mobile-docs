## SFText

The `SFText` element renders a standard text input field within a form. It supports various configurations like multiline input, validation, QR code scanning, and copy-to-clipboard functionality.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none'`, `'sentences'`, `'words'`, `'characters'` | Controls automatic capitalization. | | `'sentences'` |
| `autoCorrect` | `boolean` | Enables auto-correction. | | `true` |
| `autoFocus` | `boolean` | | | `false` |
| `backgroundColor` | `string` | Sets the background color of the input. | | `undefined` |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls the visibility of the clear button (iOS only). | | `'never'` |
| `contextualDescription` | `string` | Additional description text. | | `undefined` |
| `description` | `string` | | | `undefined` |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | If `false`, the text is not editable. | | `true` |
| `findReplace` | `{ find: string, replace: string }` | Defines find/replace rules for generating a slug displayed below the input. | | `undefined` |
| `fullWidth` | `boolean` | | | `false` |
| `hasCopy` | `boolean` | Adds a copy-to-clipboard icon/button. | | `false` |
| `hasQRScanner` | `boolean` | Adds a QR code scanner icon/button. | | `false` |
| `label` | `string` | | | `undefined` |
| `margin` | `'none'`, `'dense'`, `'normal'` | | | `'normal'` |
| `maxLength` | `number` | | | `undefined` |
| `minHeight` | `number` | | | `undefined` |
| `multiline` | `boolean` | Allows multiple lines of text input. | | `false` |
| `order` | `number` | Order of the element in the form. | | `undefined` |
| `paddingBottom` | `'none'`, `'dense'`, `'normal'` | | | `'normal'` |
| `placeholder` | `string` | | | `undefined` |
| `qrScannerParamName` | `string` | Query parameter name to extract from the scanned QR code URL. | | `'invite_code'` |
| `required` | `boolean` | | | `false` |
| `validateAction` | `string` | Action name for backend validation on blur. | | `undefined` |
| `variant` | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'`, `'livestream'` | Specifies the visual style of the component. | | `'standard'` |

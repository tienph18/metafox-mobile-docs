## AuthenticatorQrCode

Displays a QR code, typically used for setting up two-factor authentication (2FA). It shows the QR code image, a button to attempt opening a 2FA app, a manual setup key (description), and a button to copy the key.

## Visual Examples

**Variant: standard-inlined**

![Standard Inlined variant](../assets/AuthenticatorQrCode/standard-inlined.png)

**Variant: standard-outlined**

![Standard Outlined variant](../assets/AuthenticatorQrCode/standard-outlined.png)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `content` | `string` | The content/data to encode in the QR code and the URL to open 2FA apps. | Yes | `undefined` |
| `description` | `string` | | | `undefined` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | | `undefined` |
| `margin` | `'none'`, `'dense'`, `'normal'` | | | - |
| `paddingBottom` | `'none'`, `'dense'`, `'normal'` | | Yes | - |
| `placeholder` | `string` | | | `undefined` |
| `variant` | `'standard'`, `'standard-inlined'`, `'standard-outlined'` | The visual style variant of the form control. | | `'standard'` |

# AuthenticatorQrCode

Displays a QR code, typically used for setting up two-factor authentication (2FA). It shows the QR code image, a button to attempt opening a 2FA app, a manual setup key (description), and a button to copy the key.

## Props

| Name          | Type                                    | Description                                                                 | Required | Default      |
| :------------ | :-------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `label`       | `string`                                | The label displayed above the QR code section.                              | No       | `undefined`  |
| `content`     | `string`                                | The content/data to encode in the QR code and the URL to open 2FA apps.     | No       | `undefined`  |
| `description` | `string`                                | The text displayed below the QR code, typically the manual setup key.       | No       | `undefined`  |
| `placeholder` | `string`                                | The text for the button below the QR code that attempts to open 2FA apps. | No       | `undefined`  |
| `variant`     | `'standard'`, `'outlined'`, `'filled'`  | The visual style variant of the form control.                               | No       | `'standard'` |
| `margin`      | `'none'`, `'dense'`, `'normal'`         | The margin spacing for the form control.                                    | Yes      | -            |
| `paddingBottom`| `'none'`, `'dense'`, `'normal'`         | The bottom padding spacing for the form control.                            | Yes      | -            |
| `fullWidth`   | `boolean`                               | If `true`, the form control will take up the full width of its container.   | No       | `false`      |
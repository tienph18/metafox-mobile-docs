# PointConversionAmountReceived

Displays a calculated monetary amount based on a value from another form field, an exchange rate, and a fee percentage. The result is formatted according to a specified currency pattern.

## Props

| Name                | Type     | Description                                                                          | Required | Default |
| :------------------ | :------- | :----------------------------------------------------------------------------------- | :------- | :------ |
| `label`             | `string` | The base label text for the displayed amount (often an i18n key).                    | Yes      |         |
| `exchangeRate`      | `number` | The numerical exchange rate used for conversion.                                     | Yes      |         |
| `exchangeRatePattern`| `object` | An object defining the currency formatting rules (e.g., separators, precision). | Yes      |         |
| `feePercentage`     | `number` | The fee percentage to be deducted (e.g., 0.05 for 5%).                               | Yes      |         |
| `relatedField`      | `string` | The name of the form field providing the base value for the calculation.             | Yes      |         |
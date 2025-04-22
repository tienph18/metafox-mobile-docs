# SponsorCalculatorCost

This form element provides a numeric input field that calculates and displays a total cost based on the entered value, an initial unit count, and a price per unit. It's typically used for scenarios like calculating sponsorship costs based on impressions or days.

## Props

| Name                  | Type                                                          | Description                                                                 | Required | Default        |
| :-------------------- | :------------------------------------------------------------ | :-------------------------------------------------------------------------- | :------- | :------------- |
| `label`               | `string`                                                      | The display label for the form field.                                       | No       |                |
| `description`         | `string`                                                      | Additional descriptive text displayed below the input.                      | No       |                |
| `placeholder`         | `string`                                                      | Placeholder text shown when the input is empty.                             | No       |                |
| `required`            | `boolean`                                                     | Visually marks the field label as required.                                 | No       | `false`        |
| `disabled`            | `boolean`                                                     | Disables the input field.                                                   | No       | `false`        |
| `variant`             | `'standard' \| 'outlined' \| 'filled' \| 'livestream' \| 'standard-outlined'` | The visual style variant of the input field.                              | No       | `'standard'`   |
| `margin`              | `'none' \| 'dense' \| 'normal'`                               | Controls the vertical margin of the form control.                           | No       | `'normal'`     |
| `fullWidth`           | `boolean`                                                     | If `true`, the input field spans the full width of its container.           | No       | `false`        |
| `maxLength`           | `number`                                                      | Maximum number of characters allowed in the input.                          | No       |                |
| `initialUnit`         | `number`                                                      | The base unit used for the cost calculation (e.g., number of impressions).  | Yes      |                |
| `initialPrice`        | `number`                                                      | The price per `initialUnit`.                                                | Yes      |                |
| `pricePattern`        | `object`                                                      | An object defining the currency format (`symbol`, `currency_code`, etc.). | Yes      |                |
| `totalNameLabel`      | `string`                                                      | The translation key for the label prefix before the calculated total cost.  | No       | `'total_cost'` |
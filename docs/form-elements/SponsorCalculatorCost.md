## SponsorCalculatorCost

This form element provides a numeric input field that calculates and displays a total cost based on the entered value, an initial unit count, and a price per unit. It's typically used for scenarios like calculating sponsorship costs based on impressions or days.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialPrice` | `number` | The price per `initialUnit`. | Yes | |
| `initialUnit` | `number` | The base unit used for the cost calculation (e.g., number of impressions). | Yes | |
| `label` | `string` | | | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `maxLength` | `number` | | | |
| `placeholder` | `string` | | | |
| `pricePattern` | `object` | An object defining the currency format (`symbol`, `currency_code`, etc.). | Yes | |
| `required` | `boolean` | | | `false` |
| `totalNameLabel` | `string` | The translation key for the label prefix before the calculated total cost. | | `'total_cost'` |
| `variant` | `'standard' \| 'outlined' \| 'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

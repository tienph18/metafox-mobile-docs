## DynamicTypo

Displays a dynamic description text based on the value of a related form field. It looks up the description from the `config.data` array using the value of the field specified in `config.relatedField`.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `data` | `Array<{ value: any; description: string; }>` | Array of value-description pairs. | Yes | `[]` |
| `fullWidth` | `boolean` | | | |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | |
| `paddingBottom` | `'dense' \| 'normal' \| 'none'` | | | |
| `relatedField` | `string` | Name of the form field whose value determines the displayed description. | Yes | |
| `required` | `boolean` | | | |
| `variant` | `'outlined' \| 'filled' \| 'standard'` | Specifies the visual style of the component. | | |

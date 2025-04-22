# DynamicTypo

Displays a dynamic description text based on the value of a related form field. It looks up the description from the `config.data` array using the value of the field specified in `config.relatedField`.

## Props

| Name             | Type                                          | Description                                                              | Required | Default |
| :--------------- | :-------------------------------------------- | :----------------------------------------------------------------------- | :------- | :------ |
| `data`           | `Array<{ value: any; description: string; }>` | Array of value-description pairs.                                        | Yes      | `[]`    |
| `relatedField`   | `string`                                      | Name of the form field whose value determines the displayed description. | Yes      |         |
| `fullWidth`      | `boolean`                                     | Determines if the element should occupy the full width available.        | No       |         |
| `margin`         | `'dense' \| 'normal' \| 'none'`               | Specifies the margin size around the element.                            | No       |         |
| `required`       | `boolean`                                     | Indicates if the field is required (visual indicator, validation elsewhere). | No       |         |
| `variant`        | `'outlined' \| 'filled' \| 'standard'`        | The visual style variant of the element.                                 | No       |         |
| `paddingBottom`  | `'dense' \| 'normal' \| 'none'`               | Specifies the padding size below the element.                            | No       |         |
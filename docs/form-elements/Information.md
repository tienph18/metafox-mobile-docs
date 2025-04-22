# Information

Displays HTML content fetched based on the field's value, typically representing related information (e.g., a forum post).

## Props

| Name          | Type                                     | Description                                      | Required | Default     |
|---------------|------------------------------------------|--------------------------------------------------|----------|-------------|
| `fullWidth`   | `boolean`                                | Makes the control take the full available width. | No       | `false`     |
| `margin`      | `'none' \| 'dense' \| 'normal'`            | Sets the margin spacing.                         | No       | `undefined` |
| `paddingBottom`| `'none' \| 'dense' \| 'normal'`            | Sets the bottom padding spacing.                 | No       | `undefined` |
| `variant`     | `'standard' \| 'outlined' \| 'filled'`   | Sets the visual style.                           | No       | `'standard'`|
| `label`       | `string`                                 | The text label for the form element.             | Yes      |             |
| `required`    | `boolean`                                | Marks the label with an asterisk if true.        | No       | `false`     |
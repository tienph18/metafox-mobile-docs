# Range

A form element that renders a dual-handle slider, allowing users to select a range of values. It uses two separate field names (defined in `min.name` and `max.name` props) to store the selected minimum and maximum values in the form state.

## Props

| Name          | Type                                                     | Description                                                                                                | Required | Default     |
|---------------|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|-------------|
| `label`       | `string`                                                 | The label text for the form field.                                                                         | No       |             |
| `description` | `string`                                                 | Additional descriptive text displayed below the input.                                                     | No       |             |
| `required`    | `boolean`                                                | Whether the field is required. Adds a visual indicator to the label.                                       | No       | `false`     |
| `fullWidth`   | `boolean`                                                | If `true`, the component takes up the full width of its container.                                         | No       | `false`     |
| `margin`      | `'none' \| 'dense' \| 'normal'`                        | Controls the margin spacing around the component.                                                          | No       | `'normal'`  |
| `paddingBottom`| `'none' \| 'dense' \| 'normal'`                         | Controls the bottom padding of the form control wrapper.                                                   | No       |             |
| `variant`     | `'standard' \| 'outlined' \| 'filled'`                 | The visual style variant of the form control.                                                              | No       | `'standard'`|
| `step`        | `number`                                                 | The granularity that the slider can step through values.                                                   | Yes      |             |
| `min`         | `object { label: string, name: string, value: number }`  | Config for the minimum value handle. `name` is the formik field name, `value` is the slider minimum limit. | Yes      |             |
| `max`         | `object { label: string, name: string, value: number }`  | Config for the maximum value handle. `name` is the formik field name, `value` is the slider maximum limit. | Yes      |             |
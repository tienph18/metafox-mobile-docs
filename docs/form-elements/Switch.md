# Switch

A form element that renders a toggle switch input, allowing users to select between two states (on/off).

## Props

| Name                | Type                         | Description                                       | Required | Default     |
| ------------------- | ---------------------------- | ------------------------------------------------- | -------- | ----------- |
| `label`             | `string`                     | The label displayed next to the switch.           | Yes      | `undefined` |
| `description`       | `string`                     | Optional helper text displayed below the switch.  | No       | `''`        |
| `disabled`          | `boolean`                    | Disables the switch input.                        | No       | `false`     |
| `required`          | `boolean`                    | Marks the field as required.                      | No       | `false`     |
| `fullWidth`         | `boolean`                    | Makes the component take the full width available.| No       | `false`     |
| `margin`            | `'none'\|'normal'\|'dense'` | Sets the margin spacing around the component.     | No       | `'normal'`  |
| `checkedValue`      | `any`                        | The value submitted when the switch is turned on. | No       | `1`         |
| `uncheckedValue`    | `any`                        | The value submitted when the switch is turned off.| No       | `0`         |
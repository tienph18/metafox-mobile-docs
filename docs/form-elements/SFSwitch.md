# SFSwitch

A form element that renders a switch (toggle) control. It allows users to select between two states, typically representing on/off or true/false.

## Props

| Name           | Type                               | Description                                                                 | Required | Default           |
| -------------- | ---------------------------------- | --------------------------------------------------------------------------- | -------- | ----------------- |
| `label`          | string                             | The text label displayed next to the switch.                                | Yes      |                   |
| `fullWidth`      | boolean                            | If `true`, the component takes up the full width of its container.          | No       | `false`           |
| `margin`         | 'dense' \| 'normal' \| 'none'      | Defines the margin spacing around the component.                            | No       | `normal`          |
| `required`       | boolean                            | If `true`, marks the field as required.                                     | No       | `false`           |
| `variant`        | 'standard' \| 'outlined' \| 'filled' \| 'standard-inlined' | The visual style of the form control. (Note: Hardcoded to 'standard-inlined' in the component implementation) | No       | `'standard-inlined'` |
| `paddingBottom`  | 'dense' \| 'normal' \| 'none'      | Defines the bottom padding spacing for the component.                       | No       | `normal`          |
| `checkedValue`   | boolean \| number                  | The value assigned to the field when the switch is checked (on).            | No       | `1`               |
| `uncheckedValue` | boolean \| number                  | The value assigned to the field when the switch is unchecked (off).         | No       | `0`               |
| `description`    | string                             | Additional text displayed below the switch for context or instructions.     | No       | `''`              |
## SFSwitch

A form element that renders a switch (toggle) control. It allows users to select between two states, typically representing on/off or true/false.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `checkedValue` | `boolean \| number` | The value assigned to the field when the switch is checked (on). | | `1` |
| `description` | `string` | | | `''` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | `normal` |
| `paddingBottom` | `'dense' \| 'normal' \| 'none'` | | | `normal` |
| `required` | `boolean` | | | `false` |
| `uncheckedValue` | `boolean \| number` | The value assigned to the field when the switch is unchecked (off). | | `0` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | 'standard-inlined' | Specifies the visual style of the component. | | `'standard-inlined'` |

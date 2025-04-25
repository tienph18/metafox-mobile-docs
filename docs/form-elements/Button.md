## Button

A form element that renders a toggleable button. Its text changes based on its internal state (0 or 1), typically used to trigger an action or represent a binary choice within a form.

## Visual Examples

**Active State (value = 1)**

![Active State Button](../assets/Button/label-activate.png)

**Inactive State (value = 0)**

![Inactive State Button](../assets/Button/cancelabel-cancel.png)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `cancelLabel` | `string` | The text displayed on the button when its value is 0 (inactive state). | Yes | |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `true` |
| `label` | `string` | The text displayed on the button when its value is 1 (active state). | Yes | |
| `margin` | `'normal' \| 'dense' \| 'none'` | | | `'normal'` |
| `size` | `'small' \| 'medium'` | The size applied to the surrounding form control. | | `undefined` |
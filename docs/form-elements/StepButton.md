## StepButton

A button element designed for multi-step forms, allowing navigation between steps (previous/next) or form submission. It interacts with a form field (specified by `currentStepName` or defaulting to `_current_step`) to manage the active step.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `actionType` | `'previous' \| 'next' \| 'submit'` | Determines the button's behavior (navigate previous, next, or submit). | Yes | `undefined` |
| `currentStepName` | `string` | The name of the form field tracking the current step index. | | `FormStepVariable.CURRENT_KEY` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | `''` |
| `margin` | `'small' \| 'medium' \| 'large' \| 'none'` | | | `undefined` |
| `paddingBottom` | `'small' \| 'medium' \| 'large' \| 'none'` | | | `undefined` |
| `style` | `ViewStyle` | Custom styling applied to the surrounding form control. | | `undefined` |
| `variant` | `'standard' \| 'outlined'` | Specifies the visual style of the component. | | `'standard'` |

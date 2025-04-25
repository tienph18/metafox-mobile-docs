## Progress

Renders a progress bar indicating the completion status, typically used within multi-step forms. It calculates progress based on a related field (representing the current step/value) and the total number of steps/value (expected in the form context).

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `paddingLeft` | `'none' \| 'dense' \| 'normal'` | Sets the left inner padding of the form control. | | `undefined` |
| `paddingRight` | `'none' \| 'dense' \| 'normal'` | Sets the right inner padding of the form control. | | `undefined` |
| `paddingTop` | `'none' \| 'dense' \| 'normal'` | Sets the top inner padding of the form control. | | `undefined` |
| `relatedField` | `string` | The name of the form field holding the current value (e.g., current step) for progress calculation. | Yes | |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

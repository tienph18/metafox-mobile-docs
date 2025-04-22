# Progress

Renders a progress bar indicating the completion status, typically used within multi-step forms. It calculates progress based on a related field (representing the current step/value) and the total number of steps/value (expected in the form context).

## Props

| Name                | Type                                | Description                                                                                             | Required | Default      |
| :------------------ | :---------------------------------- | :------------------------------------------------------------------------------------------------------ | :------- | :----------- |
| `margin`            | `'none' \| 'dense' \| 'normal'`   | Sets the outer margin of the form control.                                                              | No       | `'normal'`   |
| `variant`           | `'standard' \| 'outlined' \| 'filled'` | The display variant of the form control.                                                              | No       | `'standard'` |
| `paddingTop`        | `'none' \| 'dense' \| 'normal'`   | Sets the top inner padding of the form control.                                                         | No       | `undefined`  |
| `paddingBottom`     | `'none' \| 'dense' \| 'normal'`   | Sets the bottom inner padding of the form control.                                                      | No       | `undefined`  |
| `paddingRight`      | `'none' \| 'dense' \| 'normal'`   | Sets the right inner padding of the form control.                                                       | No       | `undefined`  |
| `paddingLeft`       | `'none' \| 'dense' \| 'normal'`   | Sets the left inner padding of the form control.                                                        | No       | `undefined`  |
| `relatedField`      | `string`                            | The name of the form field holding the current value (e.g., current step) for progress calculation. | Yes      |              |
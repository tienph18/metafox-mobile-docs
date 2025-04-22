# StepButton

A button element designed for multi-step forms, allowing navigation between steps (previous/next) or form submission. It interacts with a form field (specified by `currentStepName` or defaulting to `_current_step`) to manage the active step.

## Props

| Name                 | Type                             | Description                                                                                   | Required | Default                     |
| :------------------- | :------------------------------- | :-------------------------------------------------------------------------------------------- | :------- | :-------------------------- |
| `label`              | `string`                         | The text displayed on the button.                                                             | Yes      | `''`                        |
| `actionType`         | `'previous' \| 'next' \| 'submit'` | Determines the button's behavior (navigate previous, next, or submit).                        | Yes      | `undefined`                 |
| `fullWidth`          | `boolean`                        | Whether the button control should occupy the full width.                                      | No       | `false`                     |
| `margin`             | `'small' \| 'medium' \| 'large' \| 'none'` | Sets the margin around the button control.                                                    | No       | `undefined`                 |
| `variant`            | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the surrounding form control.                                     | No       | `'standard'`                |
| `paddingBottom`      | `'small' \| 'medium' \| 'large' \| 'none'` | Sets the bottom padding for the form control.                                                 | No       | `undefined`                 |
| `currentStepName`    | `string`                         | The name of the form field tracking the current step index.                                   | No       | `FormStepVariable.CURRENT_KEY` |
| `style`              | `ViewStyle`                      | Custom styling applied to the surrounding form control.                                       | No       | `undefined`                 |
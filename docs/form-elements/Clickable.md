# Clickable

A form element that displays a label and a right arrow, acting as a button. When clicked, it dispatches a specified Redux action with given parameters. It's typically used to navigate to another screen or trigger a modal for further input or selection.

## Props

| Name          | Type                                       | Description                                                    | Required | Default     |
| ------------- | ------------------------------------------ | -------------------------------------------------------------- | -------- | ----------- |
| `name`        | `string`                                   | The name of the field in the form state.                       | Yes      |             |
| `label`       | `string`                                   | The text label displayed in the clickable area.                | Yes      |             |
| `action`      | `string`                                   | The Redux action type to dispatch on click.                    | Yes      |             |
| `params`      | `object`                                   | The payload to send with the dispatched action.                | Yes      |             |
| `fullWidth`   | `boolean`                                  | If true, the component takes up the full width.                | No       | `false`     |
| `margin`      | `'normal' \| 'dense' \| 'none'`            | Controls the margin around the component.                      | No       | `'normal'`  |
| `variant`     | `'standard' \| 'outlined' \| 'filled'`     | The visual style variant.                                      | No       | `'standard'`|
| `paddingBottom`| `boolean`                                  | Controls bottom padding.                                       | No       | `false`     |
| `severity`    | `'error' \| 'warning' \| 'info' \| 'success'` | Sets the text color based on severity (e.g., for validation). | No       |             |
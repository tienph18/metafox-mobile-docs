# CustomButton

A form element that renders a button which dispatches a custom Redux action when pressed.

## Props

| Name          | Type                                               | Description                                                                                                | Required | Default           |
| ------------- | -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | -------- | ----------------- |
| `name`        | `string`                                           | The unique identifier for the form field.                                                                  | Yes      | `CustomButtonField` |
| `label`       | `string`                                           | The text label displayed on the button.                                                                    | Yes      |                   |
| `variant`     | `string`                                           | Specifies the button style. Currently supports 'link'.                                                     | Yes      | `'link'`          |
| `customAction`| `{ type: string; payload?: any; meta?: any }`      | An object defining the Redux action dispatched on press. `type` is required, `payload` and `meta` are optional. | Yes      |                   |
| `disabled`    | `boolean`                                          | If true, the button is disabled.                                                                           | No       | `false`           |
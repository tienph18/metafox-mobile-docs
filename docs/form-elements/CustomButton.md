## CustomButton

A form element that renders a button which dispatches a custom Redux action when pressed.
## Visual Examples

**Default (variant: link)**

![Default Link Button](../assets/CustomButton/default.png)

### Props


| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `customAction` | `{ type: string; payload?: any; meta?: any }` | An object defining the Redux action dispatched on press. `type` is required, `payload` and `meta` are optional. | Yes | |
| `disabled` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `name` | `string` | The unique identifier for the form field. | Yes | `CustomButtonField` |
| `variant` | `string` | Specifies the button style. Currently supports 'link'. | Yes | `'link'` |

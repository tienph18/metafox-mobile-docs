# Hidden

A form element that stores a value in the form state without rendering any visible UI element. It's typically used to pass data that shouldn't be directly modified by the user.

## Props

| Name             | Type     | Description                                                              | Required | Default |
| :--------------- | :------- | :----------------------------------------------------------------------- | :------- | :------ |
| `value`          | `string` | The specific value to set for the hidden field.                          | No       | `null`  |
| `defaultValue`   | `string` | The default value to set if `config.value` is not provided.            | No       | `null`  |
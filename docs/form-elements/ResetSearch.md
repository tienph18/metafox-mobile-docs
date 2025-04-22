# ResetSearch

This element renders a button used within a search or filter form. When clicked, it resets the values of specified form fields (`targetFields`) back to their initial state as defined in the form's `initialValues`. The button is automatically hidden if the target fields currently hold their default values.

## Props

| Name           | Type     | Description                                                                 | Required | Default                           |
| -------------- | -------- | --------------------------------------------------------------------------- | -------- | --------------------------------- |
| `targetFields` | `string[]` | An array of field names within the form that this component should reset. | No       | `['sort', 'when', 'category_id']` |
| `label`        | `string` | The text label displayed on the reset button.                               | No       | `'reset'`                         |
| `title`        | `string` | A title associated with the element (specific usage may vary).              | No       | `'filter'`                        |
| `align`        | `string` | Alignment setting (specific usage may vary).                                | No       | `'right'`                         |
| `variant`      | `string` | Controls the visual style or variant of the form control wrapper.           | No       | `'standard'`                      |
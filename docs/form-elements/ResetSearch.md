## ResetSearch

This element renders a button used within a search or filter form. When clicked, it resets the values of specified form fields (`targetFields`) back to their initial state as defined in the form's `initialValues`. The button is automatically hidden if the target fields currently hold their default values.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `align` | `string` | Alignment setting (specific usage may vary). | | `'right'` |
| `label` | `string` | | | `'reset'` |
| `targetFields` | `string[]` | An array of field names within the form that this component should reset. | | `['sort', 'when', 'category_id']` |
| `title` | `string` | A title associated with the element (specific usage may vary). | | `'filter'` |
| `variant` | `string` | Specifies the visual style of the component. | | `'standard'` |

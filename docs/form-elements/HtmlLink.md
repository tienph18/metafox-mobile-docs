## HtmlLink

*Note: This element inherits most props from the base `LinkButton` element.*

For a visual reference, see [LinkButton Gallery](./form-elements/LinkButton.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `action` | `string` | A Redux action type to dispatch when the button is pressed. Takes precedence over `link` and `actionName`/`routerName`. | | |
| `actionName` | `string` | Specifies the type of navigation action (e.g., 'reset', 'navigate'). Used if `action` is not provided. | | `'navigate'` |
| `actionPayload` | `Record<string, any>` | The payload to include with the dispatched Redux action specified by `action`. | | `{}` |
| `description` | `string` | | | |
| `label` | `string` | | Yes | |
| `link` | `string` | A URL path to navigate to when the button is pressed. Used if `action` is not provided. | | |
| `margin` | `'normal'` | | Yes | |
| `routerName` | `string` | The name of the route to navigate to, used with `actionName`. Primarily for navigation actions like 'reset'. | | `'forgot-password'` |
| `textTransform` | `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'` | Controls the text transformation (e.g., uppercase, lowercase). | | |

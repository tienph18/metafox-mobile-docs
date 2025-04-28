# LinkButton

This form element renders a button styled as a link. It can be configured to navigate to a specific route/link or dispatch a Redux action upon being pressed. It's often used for actions like navigating to a "Forgot Password" screen or triggering secondary form actions.

## Props

| Name | Type | Description | Required | Default |
| :-- | :-- | :-- | :-- | :-- |
| `label` | `string` | The text displayed on the link button. | Yes |  |
| `description` | `string` | A description text displayed above the button. | |  |
| `link` | `string` | A URL path (relative) to navigate to when pressed. Takes precedence over `actionName`/`routerName` if `action` is not set. | |  |
| `action` | `string` | The type string of a Redux action to dispatch when pressed. Takes precedence over `link` and `actionName`/`routerName`. | |  |
| `actionPayload` | `Record<string, any>` | The payload object to send with the dispatched Redux `action`. | | `{}` |
| `actionName` | `'navigate' \| 'reset'` | Specifies the navigation action type. Used if `action` and `link` are not provided. | | `'navigate'` |
| `routerName` | `string` | The name of the route to navigate to. Used with `actionName`. | | `'forgot-password'` |
| `textTransform` | `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'` | CSS text-transform property for the button label. | | `'none'` |
| `margin` | `'normal'` | Controls the margin around the form control. | | `'normal'` |
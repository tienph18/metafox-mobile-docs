# HtmlLink

This element renders a button styled as a link. It's primarily used for navigation or triggering specific actions within a form, often without directly manipulating form field values. While named `HtmlLink` for consistency with web counterparts, it utilizes the `LinkButtonField` component internally for mobile implementation.

## Props

| Name          | Type                                               | Description                                                                                                                               | Required | Default             |
|---------------|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------|
| `label`       | `string`                                           | The text displayed on the button.                                                                                                         | Yes      | -                   |
| `textTransform`| `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'` | Controls the text transformation (e.g., uppercase, lowercase).                                                                            | No       | -                   |
| `margin`      | `'normal'`                                         | Specifies the margin for the form control wrapper.                                                                                        | Yes      | -                   |
| `link`        | `string`                                           | A URL path to navigate to when the button is pressed. Used if `action` is not provided.                                                   | No       | -                   |
| `routerName`  | `string`                                           | The name of the route to navigate to, used with `actionName`. Primarily for navigation actions like 'reset'.                              | No       | `'forgot-password'` |
| `actionName`  | `string`                                           | Specifies the type of navigation action (e.g., 'reset', 'navigate'). Used if `action` is not provided.                                     | No       | `'navigate'`        |
| `action`      | `string`                                           | A Redux action type to dispatch when the button is pressed. Takes precedence over `link` and `actionName`/`routerName`.                   | No       | -                   |
| `actionPayload`| `Record<string, any>`                              | The payload to include with the dispatched Redux action specified by `action`.                                                            | No       | `{}`                |
| `description` | `string`                                           | Optional text displayed below the button to provide context or instructions.                                                              | No       | -                   |
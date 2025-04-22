# GatewayButton

Renders a button specific to a payment gateway (e.g., Apple Pay, Stripe). It handles setting the selected gateway ID, passing relevant data, and triggering form submission upon click. It can display platform-specific buttons (Apple Pay/Google Pay) or a generic button based on the `variant` prop.

## Props

Props are configured via the `config` object in the form schema.

| Name             | Type                                                                               | Description                                                                                                | Required | Default    |
| :--------------- | :--------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :--------- |
| `label`          | `string`                                                                           | The text label displayed on the generic button.                                                            | Yes      |            |
| `gateway_id`     | `string \| number`                                                                 | The unique identifier for the payment gateway this button represents.                                      | Yes      |            |
| `variant`        | `'applepay' \| 'googlepay' \| 'stripe' \| 'paypal' \| 'activitypoint'`             | The type of gateway. Determines rendering logic, platform availability (Apple/Google Pay), and behavior. | Yes      |            |
| `item`           | `any`                                                                              | Item data associated with the payment, passed to the form on submission.                                   | Yes      |            |
| `gateway_config` | `any`                                                                              | Configuration specific to the selected payment gateway, passed to the form on submission.                  | Yes      |            |
| `description`    | `string`                                                                           | Optional text description displayed below the button.                                                      | No       | `''`       |
| `icon`           | `string`                                                                           | Optional icon name (from the icon set) to display on the generic button.                                   | No       |            |
| `confirmation`   | `{ title: string, message: string }`                                               | Optional configuration for a confirmation dialog shown before submission (used for `activitypoint` variant). | No       |            |
| `disabled`       | `boolean`                                                                          | If `true`, the button is disabled and cannot be pressed.                                                   | No       | `false`    |
| `fullWidth`      | `boolean`                                                                          | If `true`, the underlying form control takes the full available width.                                     | No       | `true`     |
| `margin`         | `'none' \| 'dense' \| 'normal' \| 'small'`                                         | Margin size applied to the underlying form control.                                                        | No       | `'none'`   |
| `size`           | `'small' \| 'medium' \| 'large'`                                                   | Size applied to the underlying form control (affects spacing/layout).                                      | No       |            |
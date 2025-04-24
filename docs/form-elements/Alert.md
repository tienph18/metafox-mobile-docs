## Alert

Displays a styled alert box containing an HTML message. The appearance (color, icon) depends on the `severity` and `variant`.

## Visual Examples

**Severity: info (default)**

![Severity Info](../assets/Alert/severity-info.png)

**Severity: success**

![Severity Success](../assets/Alert/severity-success.png)

**Severity: warning**

![Severity Warning](../assets/Alert/severity-warning.png)

**Severity: error**

![Severity Error](../assets/Alert/severity-error.png)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `message` | `string` | The HTML content to display in the alert. | Yes | |
| `severity` | `'success' \| 'info' \| 'warning' \| 'error'` | Change icon by the alert type (info, success, warning, error). | | `'info'` |
| `variant` | `'standard'` | Controls the overall style variant of the alert. | | `'standard'` |


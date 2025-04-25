## SocialButtons

This element renders a container for multiple social login buttons. It dynamically adjusts the layout based on the number of buttons: displaying them in a row if there are more than two, and stacked vertically otherwise. It also handles platform-specific visibility, hiding the Apple login button on Android devices.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `elements` | `Record<string, any>` | Configuration objects for each individual social button element. | Yes | |
| `totalButton` | `number` | The total count of configured social buttons, used to determine layout. | Yes | |

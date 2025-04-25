## AvatarUpload

A form element that allows users to select and upload an avatar image, displaying a preview. It integrates with the device's image picker and handles basic validation display.

## Visual Examples
 
**Circle: true (Default)**
 
![Circle True](../assets/AvatarUpload/circle-true.png)
 
**Circle: false**
 
![Circle False](../assets/AvatarUpload/circle-false.png)
 
**Space Color: green & Space Width: 1**
 
![Space Color Green](../assets/AvatarUpload/spaceColor-green.png)
 
### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `borderColor` | `string` | Color of the border around the avatar image. | | `undefined` |
| `circle` | `boolean` | Renders the avatar preview as a circle. | | `true` |
| `fullWidth` | `boolean` | | | `false` |
| `margin` | `keyof typeof SizeEnum` | | | `'none'` |
| `paddingBottom` | `keyof typeof SizeEnum` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `size` | `string` | Size of the avatar preview (e.g., 'small', 'medium', 'xxlarge'). | | `'xxlarge'` |
| `spaceColor` | `string` | Color of the space around the avatar image. | | `undefined` |
| `spaceWidth` | `number` | Width of the space around the avatar image. | | `undefined` |

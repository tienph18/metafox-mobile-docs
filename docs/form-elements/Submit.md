## Submit

A button element used to trigger form submission. It integrates with Formik to handle the submit action and can be configured with various visual styles and behaviors.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `color` | `'primary' \| 'secondary' \| 'error' \| 'warning' \| 'info' \| 'success' \| 'inherit' \| string` | The color of the button. Defaults to 'gray' when disabled. | | `'primary'` |
| `customAction` | `{ type: string; payload?: any }` | Dispatches a custom Redux action when the button is clicked after submitting the form. | | |
| `disableWhenClean` | `boolean` | If true, the button is disabled when the form is pristine (no changes made). | | `false` |
| `disabled` | `boolean` | | | `false` |
| `first` | `boolean` | Style adjustment if it's the first element in a group. | | `false` |
| `fontWeight` | `'light' \| 'regular' \| 'medium' \| 'bold'` | The font weight of the button text. | | |
| `fullWidth` | `boolean` | | | `false` |
| `icon` | `string` | Name of the icon to display on the button. | | |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `outline` | `boolean` | Applies an outline style to the button. | | `false` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `round` | `boolean` | If true, makes the button round (intended for icon buttons). | | `false` |
| `size` | `'small' \| 'medium' \| 'large' \| 'string'` | The size of the button. Note: The component internally uses 'normal'. | | `'medium'` |
| `style` | `object` | Custom styles to apply to the FormControl container. | | |
| `textTransform` | `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'` | Controls the text transformation (e.g., uppercase). | | |
| `transparent` | `boolean` | Makes the button background transparent. | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'contained'` | Specifies the visual style of the component. | | `'standard'` |

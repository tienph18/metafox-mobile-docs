# SearchBox

A form element intended for search input fields. Currently, this component displays a "Coming Soon" placeholder, indicating the feature is under development.

## Props

| Name             | Type      | Description                                                     | Required | Default    |
| :--------------- | :-------- | :-------------------------------------------------------------- | :------- | :--------- |
| `placeholder`      | `string`  | Placeholder text displayed in the search input when empty.      | No       |            |
| `size`             | `string`  | Defines the size of the input field (e.g., 'small', 'medium').  | No       |            |
| `margin`           | `string`  | Specifies the margin around the form control ('none', 'normal', 'dense'). | No       | `'normal'` |
| `fullWidth`        | `boolean` | If `true`, the input field will occupy the full available width.  | No       | `true`     |
| `className`        | `string`  | An optional CSS class name to apply to the component for styling. | No       |            |
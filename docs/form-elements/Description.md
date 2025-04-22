# Description

Displays a simple text label within a form, often used for informational purposes or section descriptions.

## Props

| Name          | Type                     | Description                                      | Required | Default      |
| ------------- | ------------------------ | ------------------------------------------------ | -------- | ------------ |
| `label`       | `string`                 | The text content to display.                     | Yes      |              |
| `variant`     | `keyof typeof Variant`   | The visual style variant (e.g., 'standard').     | No       | `'standard'` |
| `fullWidth`   | `boolean`                | Determines if the element takes up full width.   | No       | `false`      |
| `margin`      | `keyof typeof SizeEnum`  | Sets the margin around the element.              | No       | `undefined`  |
| `paddingBottom`| `keyof typeof SizeEnum`  | Sets the bottom padding of the element.          | No       | `undefined`  |
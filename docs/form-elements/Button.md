# Button

A form element that renders a toggleable button. Its text changes based on its internal state (0 or 1), typically used to trigger an action or represent a binary choice within a form.

## Props

| Name          | Type                             | Description                                                                 | Required | Default    |
|---------------|----------------------------------|-----------------------------------------------------------------------------|----------|------------|
| label         | `string`                         | The text displayed on the button when its value is 1 (active state).        | Yes      |            |
| cancelLabel   | `string`                         | The text displayed on the button when its value is 0 (inactive state).      | Yes      |            |
| disabled      | `boolean`                        | If `true`, disables the button interaction.                                 | No       | `false`    |
| fullWidth     | `boolean`                        | If `true`, the surrounding form control takes up the full available width.  | No       | `true`     |
| margin        | `'normal' \| 'dense' \| 'none'` | The margin applied to the surrounding form control.                         | No       | `'normal'` |
| size          | `'small' \| 'medium'`          | The size applied to the surrounding form control.                           | No       | `undefined`|
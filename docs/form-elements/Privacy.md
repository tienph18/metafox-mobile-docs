# Privacy

This element provides a user interface for selecting privacy settings, typically used for controlling who can see a piece of content (e.g., a post). It displays the currently selected privacy option (with an icon and label) and opens a dedicated selector view (`SelectPrivacyView`) when tapped.

## Props

| Name             | Type                                  | Description                                                                 | Required | Default            |
| :--------------- | :------------------------------------ | :-------------------------------------------------------------------------- | :------- | :----------------- |
| `label`          | `string`                              | The text label displayed for the form field.                                | Yes      |                    |
| `options`        | `PrivacyOptionItemShape[]`            | An array of predefined privacy options available for selection.             | Yes      | `[]`               |
| `name`           | `string`                              | The unique identifier for the field within the form.                        | Yes      |                    |
| `fullWidth`      | `boolean`                             | If `true`, the component will occupy the full width of its container.       | No       | `false`            |
| `margin`         | `'dense' \| 'normal' \| 'none'`       | Specifies the margin spacing around the component.                          | No       | `'normal'`         |
| `required`       | `boolean`                             | If `true`, the field must have a value for form submission.                 | No       | `false`            |
| `variant`        | `'standard' \| 'outlined' \| 'filled' \| 'standard-inlined' \| 'livestream'` | The visual style variant of the component.                                  | No       | `'standard-inlined'` |
| `suboptions`     | `SubOptionsShape`                     | Additional options, often used for custom privacy lists or friend lists.    | No       | `[]`               |
| `disable_custom` | `boolean`                             | If `true`, prevents users from selecting custom privacy options.            | No       | `false`            |
| `multiple`       | `boolean`                             | If `true`, allows selecting multiple privacy options (currently single).    | No       | `false`            |
| `paddingBottom`  | `'dense' \| 'normal' \| 'none'`       | Specifies the bottom padding spacing for the component.                     | No       | `undefined`        |
| `description`    | `string`                              | Additional helper text displayed below the input field.                     | No       | `undefined`        |
| `disabled`       | `boolean`                             | If `true`, the field is non-interactive.                                    | No       | `false`            |
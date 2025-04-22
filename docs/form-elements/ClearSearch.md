# ClearSearch

This element displays a title and a conditional "Reset" button within a form. The button allows users to reset specific form fields (defined by `targetFields`) back to their initial values. The button only appears when the current values of the target fields differ from their initial state.

## Props

| Name           | Type     | Description                                                                              | Required | Default                             |
| -------------- | -------- | ---------------------------------------------------------------------------------------- | -------- | ----------------------------------- |
| `targetFields` | `string[]` | An array of form field names that this element will reset when the button is pressed.    | No       | `['sort', 'when', 'category_id']` |
| `label`        | `string` | The localization key for the text displayed on the reset button.                         | No       | `'reset'`                           |
| `title`        | `string` | The localization key for the title displayed above the reset button.                     | No       | `'filter'`                          |
| `align`        | `string` | Alignment configuration (appears unused in the current implementation).                  | No       | `'right'`                           |
# SFSearchBox

The `SFSearchBox` component renders a search input field integrated directly into the screen's header navigation bar. It automatically handles focus, clearing, and debounced value updates for form submission.

## Props

The component accepts standard `FormFieldProps` (`name`, `config`, `disabled`, `formik`). The primary configuration is done via the `config` object:

| Name             | Type                                                          | Description                                       | Required | Default         |
| :--------------- | :------------------------------------------------------------ | :------------------------------------------------ | :------- | :-------------- |
| `placeholder`    | `string`                                                      | Placeholder text for the input.                   | No       | `undefined`     |
| `clearButtonMode`| `'never' \| 'while-editing' \| 'unless-editing' \| 'always'`  | How the clear button behaves (iOS only).          | No       | `undefined`     |
| `editable`       | `boolean`                                                     | If the input is editable.                         | No       | `true`          |
| `required`       | `boolean`                                                     | If the field is required.                         | No       | `false`         |
| `variant`        | `keyof typeof Variant`                                        | Visual style variant.                             | No       | `undefined`     |
| `multipleline`   | `boolean`                                                     | If the input allows multiple lines.               | No       | `false`         |
| `showSearchIcon` | `boolean`                                                     | Whether to show the search icon.                  | No       | `true`          |
| `fullWidth`      | `boolean`                                                     | If the component should take full width.          | No       | `false`         |
| `margin`         | `keyof typeof SizeEnum`                                       | Margin size.                                      | No       | `undefined`     |
| `paddingBottom`  | `keyof typeof SizeEnum`                                       | Bottom padding size.                              | No       | `undefined`     |
| `minHeight`      | `number`                                                      | Minimum height of the input.                      | No       | `undefined`     |
| `maxLength`      | `number`                                                      | Maximum input length.                             | No       | `undefined`     |
| `autoCorrect`    | `boolean`                                                     | Enable/disable auto-correction.                   | No       | `false`         |
| `autoCapitalize` | `'none' \| 'sentences' \| 'words' \| 'characters'`            | Auto-capitalization behavior.                     | No       | `'none'`        |
| `autoFocus`      | `boolean`                                                     | If the input should auto-focus on mount.          | No       | `true` if empty |
| `description`    | `string`                                                      | Description text (not directly rendered by default). | No       | `undefined`     |
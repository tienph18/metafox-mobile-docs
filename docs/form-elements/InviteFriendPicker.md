# InviteFriendPicker

A form element that allows users to select one or multiple friends to invite, typically fetching suggestions from an API endpoint. It opens a dedicated selection screen.

## Props

| Name            | Type                      | Description                                                      | Required | Default      |
| --------------- | ------------------------- | ---------------------------------------------------------------- | -------- | ------------ |
| `label`         | `string`                  | The label text displayed for the field.                          | Yes      | `''`         |
| `api_endpoint`  | `string`                  | API endpoint URL to fetch friend suggestions.                    | Yes      | `''`         |
| `fullWidth`     | `boolean`                 | If `true`, the element takes the full width of its container.    | No       | `false`      |
| `margin`        | `'none' \| 'dense' \| 'normal'` | Controls the margin spacing around the element.                  | No       | `'normal'`   |
| `required`      | `boolean`                 | If `true`, the field must have a value.                          | No       | `false`      |
| `variant`       | `'standard' \| 'outlined' \| 'filled'` | The display style variant of the form control.                 | No       | `'standard'` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | Controls the bottom padding spacing.                             | No       | `'normal'`   |
| `suboptions`    | `SubOptionsShape`         | Configuration for sub-options within the picker.                 | No       | `undefined`  |
| `disable_custom`| `boolean`                 | If `true`, disables the custom privacy/selection option.         | No       | `false`      |
| `multiple`      | `boolean`                 | If `true`, allows selecting multiple friends.                    | No       | `false`      |
| `enable_search` | `boolean`                 | If `true`, enables search functionality within the picker screen. | No       | `false`      |
| `disable_uncheck`| `boolean`                 | If `true`, prevents users from unselecting chosen options.       | No       | `false`      |
| `choice_type`   | `string`                  | Specifies the type of choice (internal use).                     | No       | `''`         |
| `placeholder`   | `string`                  | Text displayed when no value is selected.                        | No       | `''`         |
| `api_params`    | `Record<string, any>`     | Additional parameters sent with the API request.                 | No       | `{ q: ':q' }`|
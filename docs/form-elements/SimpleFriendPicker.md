# SimpleFriendPicker

A form element that allows users to select one or multiple friends from a searchable list. It displays selected friends as chips and provides an interface to browse and search all available friends fetched via API.

## Props

| Name             | Type                                  | Description                                       | Required | Default                          |
| :--------------- | :------------------------------------ | :------------------------------------------------ | :------- | :------------------------------- |
| `fullWidth`      | `boolean`                             | If `true`, the component takes up the full width. | No       | `false`                          |
| `margin`         | `'none' \| 'dense' \| 'normal'`       | Defines the margin spacing around the element.    | No       | `'normal'`                       |
| `required`       | `boolean`                             | If `true`, the field must have a value.           | No       | `false`                          |
| `variant`        | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the input field.      | No       | `'standard'`                     |
| `paddingBottom`  | `'none' \| 'dense' \| 'normal'`       | Defines the bottom padding spacing.               | No       | `undefined`                      |
| `label`          | `string`                              | The label text for the form field.                | No       | `''`                             |
| `initialValue`   | `OptionsItemShape[]`                  | An array of initially selected friend objects.    | No       | `[]`                             |
| `multiple`       | `boolean`                             | If `true`, allows selecting multiple friends.     | No       | `false`                          |
| `placeholder`    | `string`                              | Placeholder text for the search input field.      | No       | `'Search friends by their name'` |
| `onFocus`        | `(event: any) => void`                | Callback function triggered when the input focuses. | No       | `undefined`                      |
## SimpleFriendPicker

A form element that allows users to select one or multiple friends from a searchable list. It displays selected friends as chips and provides an interface to browse and search all available friends fetched via API.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `OptionsItemShape[]` | An array of initially selected friend objects. | | `[]` |
| `label` | `string` | | | `''` |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `multiple` | `boolean` | If `true`, allows selecting multiple friends. | | `false` |
| `onFocus` | `(event: any) => void` | Callback function triggered when the input focuses. | | `undefined` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `placeholder` | `string` | | | `'Search friends by their name'` |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |
